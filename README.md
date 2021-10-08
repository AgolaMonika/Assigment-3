# Assigment-3
print("Enter Choice between 1 to 3")
var c=Int(readLine(strippingNewline: true)!)

switch c{
  case 1:
    print("Number Right Triangle")
    print("Enter number of row ")
    var n=Int(readLine() ?? "0") ?? 0
    
    for i in 1...n{
      for j in 1...i{
        print("\(j)", terminator: " ")
      }
      print("\n")
    }
    break
  case 2:
    print("Sequential Number Right Triangle")
    print("Enter number of row ")
    var n=Int(readLine() ?? "0") ?? 0
    var k=1
    for i in 1...5{
      for j in 1...i{
        print(" \(k)", terminator: " ")
        k=k+1
      }
      print("\n")
    }
    break
  case 3:
    print("Pascal Triangle")
    print("Enter number of row ")
    var n=Int(readLine() ?? "0") ?? 0
    var temp=1
    var num=1
    var den=1
    for i in 0...n-1{
      temp=1;
      num=i
      den=1
      for j in 0...i{
        print("\(temp)",terminator:" ")
        temp=temp*num
        temp=temp/den
        num=num-1
        den=den+1
      }
      print()
    }
    break
  default:
    print("Invalid choice")
    break
}

