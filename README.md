# SymbolTextLabel-iOS-Swift
SymbolTextLabel can be used for lists to add bullets or other symbol codes to list items. You can set font size and spacing between the symbol and text 


Example:

1. Download and copy SymbolTextLabel.swift and SymbolTextLabel.xib files inside your project
2. In your View Controller scene in storyboard/Interface Builder, drag and drop the UIView from the object library and connect the outlets (Dont set the height or the height constraint).
3. For more Details follow the code: ->

import UIKit

class ViewController: UIViewController {

    @IBOutlet var view: UiView!
    
    var testString = "Understanding the concept of sales"
    var bulletSymbol = "\u{2022}"
    var fontsize: CGFloat = 18

    override func viewDidLoad() {
        super.viewDidLoad()
        
        let symbolTextLabel = SymbolTextLabel(frame: CGRect(x: 0, y: 0, width: 0, height: 0))
        symbolTextLabel.setText(text: testString, symbolCode: bulletSymbol) //setting text and symbol of text item
        symbolTextLabel.setFontSize(textSize: fontsize) // setting font size
        //symbolTextLabel.setSpacing(spacing: 5) // setting space between symbol and text
        
        view.addSubview(symbolTextLabel)
        
    }
}
