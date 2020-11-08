---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275166"
---
# <span data-ttu-id="a1c60-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="a1c60-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="a1c60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1c60-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c60-103">Destek bileti iletişimi alın.</span><span class="sxs-lookup"><span data-stu-id="a1c60-103">Get support ticket communications.</span></span>

## <span data-ttu-id="a1c60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1c60-104">SYNTAX</span></span>

### <span data-ttu-id="a1c60-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1c60-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1c60-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1c60-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1c60-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1c60-107">DESCRIPTION</span></span>
<span data-ttu-id="a1c60-108">Destek bileti için iletişimleri alır.</span><span class="sxs-lookup"><span data-stu-id="a1c60-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="a1c60-109">Başka parametre belirtmezseniz, bir bilet için tüm iletişimleri alır.</span><span class="sxs-lookup"><span data-stu-id="a1c60-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="a1c60-110">Ayrıca, Filter parametresini kullanarak da iletişim için CreatedDate veya CommunicationType ile iletişime filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1c60-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="a1c60-111">Burada, belirleyebileceğiniz filtre değerlerine örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a1c60-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="a1c60-112">Vurgu</span><span class="sxs-lookup"><span data-stu-id="a1c60-112">Scenario</span></span>                                                        | <span data-ttu-id="a1c60-113">Filtreleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a1c60-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a1c60-114">Web iletişimi alma</span><span class="sxs-lookup"><span data-stu-id="a1c60-114">Get Web communications</span></span>                                          | <span data-ttu-id="a1c60-115">"CommunicationType EQ ' Web '"</span><span class="sxs-lookup"><span data-stu-id="a1c60-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="a1c60-116">Telefon iletişimlerini alın</span><span class="sxs-lookup"><span data-stu-id="a1c60-116">Get Phone communications</span></span>                                        | <span data-ttu-id="a1c60-117">"CommunicationType EQ ' telefon '"</span><span class="sxs-lookup"><span data-stu-id="a1c60-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="a1c60-118">20 ' nin üstünde veya altında oluşturulmuş iletişimi 2019</span><span class="sxs-lookup"><span data-stu-id="a1c60-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="a1c60-119">"CreatedDate Ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="a1c60-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="a1c60-120">20 ' den sonra oluşturulan iletişimi alma, 2019</span><span class="sxs-lookup"><span data-stu-id="a1c60-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="a1c60-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="a1c60-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="a1c60-122">20 ' den sonra oluşturulan Web iletişimlerini alır, 2019</span><span class="sxs-lookup"><span data-stu-id="a1c60-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="a1c60-123">"CreatedDate gt 2019-12-20 ve CommunicationType EQ ' Web '"</span><span class="sxs-lookup"><span data-stu-id="a1c60-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="a1c60-124">Bu cmdlet öncelikle sayfalamayı destekler ve parametreleri atlar.</span><span class="sxs-lookup"><span data-stu-id="a1c60-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="a1c60-125">İletişim adını belirterek tek bir destek bileti de alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1c60-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="a1c60-126">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1c60-126">EXAMPLES</span></span>

### <span data-ttu-id="a1c60-127">Örnek 1: destek bileti için tüm iletişimleri alma</span><span class="sxs-lookup"><span data-stu-id="a1c60-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="a1c60-128">Örnek 2: destek bileti adına göre tek bir iletişimi alma</span><span class="sxs-lookup"><span data-stu-id="a1c60-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="a1c60-129">Örnek 3: destek bileti için ilk 2 iletişimi alma</span><span class="sxs-lookup"><span data-stu-id="a1c60-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a1c60-130">Örnek 4: destek bileti için ilk 2 iletişimin atlandıktan sonraki 2 iletişimi alma</span><span class="sxs-lookup"><span data-stu-id="a1c60-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a1c60-131">Örnek 5: destek bileti için tüm Web iletişimlerini alma</span><span class="sxs-lookup"><span data-stu-id="a1c60-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a1c60-132">Örnek 6: destek bileti için 2019 tarihinde veya daha sonra oluşturulan tüm iletişimleri alma</span><span class="sxs-lookup"><span data-stu-id="a1c60-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a1c60-133">Örnek 7: destek bileti için 2019 tarihinde veya daha sonra oluşturulan tüm Web iletişimlerini alın</span><span class="sxs-lookup"><span data-stu-id="a1c60-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="a1c60-134">Örnek 8: destek bileti için destek bileti</span><span class="sxs-lookup"><span data-stu-id="a1c60-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="a1c60-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1c60-135">PARAMETERS</span></span>

### <span data-ttu-id="a1c60-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c60-136">-DefaultProfile</span></span>
<span data-ttu-id="a1c60-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1c60-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-138">-Filtre</span><span class="sxs-lookup"><span data-stu-id="a1c60-138">-Filter</span></span>
<span data-ttu-id="a1c60-139">Bu cmdlet 'in sonuçlarına uygulanacak filtre.</span><span class="sxs-lookup"><span data-stu-id="a1c60-139">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1c60-140">-Name</span></span>
<span data-ttu-id="a1c60-141">İletişim adı.</span><span class="sxs-lookup"><span data-stu-id="a1c60-141">Communication name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-142">-Supportbilet adı</span><span class="sxs-lookup"><span data-stu-id="a1c60-142">-SupportTicketName</span></span>
<span data-ttu-id="a1c60-143">Destek bileti adı.</span><span class="sxs-lookup"><span data-stu-id="a1c60-143">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="a1c60-144">-SupportTicketObject</span></span>
<span data-ttu-id="a1c60-145">Destek bileti nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a1c60-145">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-146">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="a1c60-146">-IncludeTotalCount</span></span>
<span data-ttu-id="a1c60-147">Veri kümesindeki toplam nesne sayısını (tamsayı) ve ardından seçilen nesneleri raporlar.</span><span class="sxs-lookup"><span data-stu-id="a1c60-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="a1c60-148">Cmdlet toplam sayısını belirleyemiyorsa, "bilinmeyen toplam sayı" görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a1c60-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="a1c60-149">Tamsayı, toplam sayı değerinin güvenilirliğini belirten bir doğruluk özelliğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="a1c60-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="a1c60-150">0,0 ile 0,0 1,0 arasındaki doğruluk değeri aralığı, cmdlet 'in nesneleri saymadığı anlamına gelir; 1,0, Count 'un tam olduğu ve 0,0 ile 1,0 arasındaki bir değer giderek gittikçe güvenilir bir tahmini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="a1c60-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-151">-Atla</span><span class="sxs-lookup"><span data-stu-id="a1c60-151">-Skip</span></span>
<span data-ttu-id="a1c60-152">Belirtilen sayıda nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="a1c60-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="a1c60-153">Atlanacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="a1c60-153">Enter the number of objects to skip.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-154">-Önce</span><span class="sxs-lookup"><span data-stu-id="a1c60-154">-First</span></span>
<span data-ttu-id="a1c60-155">Yalnızca belirtilen sayıda nesneyi alır.</span><span class="sxs-lookup"><span data-stu-id="a1c60-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="a1c60-156">Alınacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="a1c60-156">Enter the number of objects to get.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c60-157">CommonParameters</span></span>
<span data-ttu-id="a1c60-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1c60-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c60-159">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a1c60-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c60-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1c60-160">INPUTS</span></span>

### <span data-ttu-id="a1c60-161">Microsoft. Azure. Commands. support. model. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="a1c60-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="a1c60-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1c60-162">OUTPUTS</span></span>

### <span data-ttu-id="a1c60-163">Microsoft. Azure. Commands. support. model. Pssupportfcommunication Iletişimi</span><span class="sxs-lookup"><span data-stu-id="a1c60-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="a1c60-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1c60-164">NOTES</span></span>

## <span data-ttu-id="a1c60-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1c60-165">RELATED LINKS</span></span>
