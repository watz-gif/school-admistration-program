import csv

def write_into_csv(info_list):
                with open('student_info.csv', 'a', newline='') as csv_file:
                                #basically writing a ensures that a new a new file is not created everytime 
                                writer=csv.writer(csv_file)
                                #basically this pary ensures that the name and other headlines dont often everytime

                                if csv_file.tell()==0:
                                     writer.writerow(["Name","Age", "Contact no","Email id"])
                                     
                                writer.writerow(info_list)

if __name__=='_main_':

     condition=True
     student_num = 1

     while(condition):
                student_info=input("Enter student infromation for student #{}in the following format (Name Age Contact_Number Email_ID)".format(student.num))
                

                #split
                student_info_list = student_info.split(' ')
                

                print("\nThe entered information is -\nName: {}\nAge:{}\nContact_number: {}\nE-mail ID:{}"
                      .format(student_info_list[0],student_info_list[1],student_info_list[2],student_info_list[3]))             

                choice_check=input("is the printed information correct?(yes/no):")

                if choice_check == "yes":
                                   write_into_csv(student_info_list)
                                   condition_check=input("Enter(yes/no) if you want to enter information for another student")
                                   if condition_check == "yes":
                                        condition = True
                                        student_num = student_num + 1
                                   elif condition_check == "no":
                                        condition = False
                elif choice_check == "no":
                     print("\nRenter the Values")
                                
