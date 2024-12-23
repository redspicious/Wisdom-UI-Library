Main UI Creation

local main = Library.Main("Random Hub")

    Function: Creates the main window of the GUI with the specified name.
    Parameters:
        title (string): The title of the main window (e.g., "Random Hub").
    Returns: The main object used to create tabs and other UI elements.

Sidebar Creation

local sideBar = main.createSidebar(false)

    Function: Creates a sidebar for the main window.
    Parameters:
        scrollingEnabled (boolean): Whether the sidebar is a scrolling frame  or not (false means normal frame, true means scrolling frame).
    Returns: The sideBar object used to create tabs.

Tabs Creation

local mainTab = sideBar.createTab("Main", "rbxassetid://")
local playerTab = sideBar.createTab("Player", "rbxassetid://")

    Function: Creates tabs in the sidebar.
    Parameters:
        title (string): The title of the tab (e.g., "Main", "Player").
        icon (string): The asset ID for the icon displayed on the tab.
    Returns: The tab object (mainTab or playerTab) used to add elements inside the tab.

Button Creation

local printButton = mainTab.createButton("Button", function()
    print("Button clicked!")
end)

    Function: Creates a button inside a tab.
    Parameters:
        label (string): The text on the button (e.g., "Button").
        callback (function): The function to be executed when the button is clicked.
    Returns: The printButton object representing the created button.

Label Creation

local statusLabel = mainTab.createLabel("Label")

    Function: Creates a label inside a tab.
    Parameters:
        text (string): The text to display on the label (e.g., "Label").
    Returns: The statusLabel object representing the created label.

Input Field Creation

local input = mainTab.createInput("Input", 0.5, function(value)
    print(value)
end)

    Function: Creates an input field (e.g., text box or number box).
    Parameters:
        label (string): The label for the input field (e.g., "Input").
        default (number): The default value for the input (e.g., 0.5).
        callback (function): The function executed when the user changes the input value.
    Returns: The input object representing the created input field.

Toggle Creation

local toggle = mainTab.createToggle("Toggle", function(status)
    if status then
        print("Enabled")
    else
        print("Disabled")
    end
end)

    Function: Creates a toggle switch (checkbox-like UI element).
    Parameters:
        label (string): The label for the toggle (e.g., "Toggle").
        callback (function): The function executed when the toggle is changed. It passes a status boolean indicating whether the toggle is enabled (true) or disabled (false).
    Returns: The toggle object representing the created toggle.

Slider Creation

local slider = mainTab.createSlider("Slider", 0, 16, 500, function(value)
    print("Slider set to:", value)
end)

    Function: Creates a slider element.
    Parameters:
        label (string): The label for the slider (e.g., "Slider").
        min (number): The minimum value for the slider (e.g., 0).
        default (number): The default value of the slider (e.g., 16).
        max (number): The maximum value for the slider (e.g., 500).
        callback (function): The function executed when the slider value changes.
    Returns: The slider object representing the created slider.

Dropdown Creation

local dropdownList = {"Hello1", "Hello2", "Hello3"}
local dropdown = mainTab.createDropdown("Print Selection", dropdownList, function(input)
    selectedPrint = input
    print(selectedPrint)
end)

    Function: Creates a dropdown menu.
    Parameters:
        label (string): The label for the dropdown (e.g., "Print Selection").
        options (table): A table containing the list of dropdown options (e.g., {"Hello1", "Hello2", "Hello3"}).
        callback (function): The function executed when an option is selected. It passes the selected value as input.
    Returns: The dropdown object representing the created dropdown.

yes i used chatgpt for this cause i dont have time to make a well thought out documentation sorry lol (and im lazy)
