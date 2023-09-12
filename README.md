# IOS-App
class


//prints pop up message use this code:
        
        let alertController = UIAlertController(title: "You Must be Rich", message: "Hello there", preferredStyle: UIAlertController.Style.alert)
        
        alertController.addAction(UIAlertAction(title: "ok", style: UIAlertAction.Style.default, handler: nil))
        
        present(alertController,animated: true,completion: nil)



// Useing tip with diffrent settings:
       
        let userInput = Float(TxtBillAmount.text!)
        let index : Int = DifTipAmout.selectedSegmentIndex
        var TipRate : Float
        if index == 0 {
            TipRate = 0.15
        }
        else if index == 1 {
            TipRate = 0.20
        }
        else {
            TipRate = 0.25
        }
        let Tip = userInput! * TipRate
        
        let dispay = String(format:"$%.2f",Tip)
        
        LblTipamount.text = dispay
        }

//this click away anaything on screen:
    
    override func touchesBegan(_ touches: Set<UITouch>, with event: UIEvent?) {
        self.view.endEditing(true)
    }
        
