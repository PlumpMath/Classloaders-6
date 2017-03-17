Ваша задача написать загрузчик плагинов в вашу систему. Допустим вы пишите свой браузер и хотите чтобы люди имели имели возможность писать плагины для него. 
Соответственно, разные разработчики могут назвать свои классы одинаковым именем, ваш загрузчик должен корректно это обрабатывать. 

Задача реализовать следующий класс.
package ru.sbt;

public class PluginManager {
    private final String pluginRootDirectory;

    public PluginManager(String pluginRootDirectory) {
        this.pluginRootDirectory = pluginRootDirectory;
    }

    public Plugin load(String pluginName, String pluginClassName) {
        //todo
    }
}


Plugin - это базовый интерфейс  для всех плагинов
public interface Plugin {
    //methods doesn't matter
    void doUsefull();
}
}
PluginManager ищет скомпилированные классы плагина в папке pluginRootDirectory\pluginName\
