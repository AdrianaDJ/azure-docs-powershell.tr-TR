---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 625d5e375a8a0e7ad2af5256fc344d80a240d37d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937805"
---
# <span data-ttu-id="9ecbb-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9ecbb-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="9ecbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ecbb-102">SYNOPSIS</span></span>
<span data-ttu-id="9ecbb-103">Destek biletlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-103">Get support tickets.</span></span>

## <span data-ttu-id="9ecbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ecbb-104">SYNTAX</span></span>

### <span data-ttu-id="9ecbb-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ecbb-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9ecbb-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ecbb-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="9ecbb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ecbb-107">DESCRIPTION</span></span>
<span data-ttu-id="9ecbb-108">Destek biletleri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-108">Gets the list of support tickets.</span></span> <span data-ttu-id="9ecbb-109">Herhangi bir parametre belirtmezseniz tüm destek biletlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="9ecbb-110">Ayrıca, filtre parametresini kullanarak destek biletlerini duruma veya CreatedDate 'e göre de filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="9ecbb-111">Burada, belirleyebileceğiniz filtre değerlerine örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="9ecbb-112">Vurgu</span><span class="sxs-lookup"><span data-stu-id="9ecbb-112">Scenario</span></span>                                                         | <span data-ttu-id="9ecbb-113">Filtreleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9ecbb-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="9ecbb-114">Açık durumda olan anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="9ecbb-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="9ecbb-115">"Durum EQ ' Aç '"</span><span class="sxs-lookup"><span data-stu-id="9ecbb-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="9ecbb-116">Kapatma durumundaki anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="9ecbb-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="9ecbb-117">"Durum EQ ' kapandı '"</span><span class="sxs-lookup"><span data-stu-id="9ecbb-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="9ecbb-118">20 ' nin üstünde veya altında oluşturulmuş anahtarları 2019</span><span class="sxs-lookup"><span data-stu-id="9ecbb-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="9ecbb-119">"CreatedDate Ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="9ecbb-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="9ecbb-120">20 ' den sonra oluşturulmuş anahtarları alın, 2019</span><span class="sxs-lookup"><span data-stu-id="9ecbb-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="9ecbb-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="9ecbb-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="9ecbb-122">20 2019 ' den sonra oluşturulan anahtarları alır; açık durumda.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="9ecbb-123">"CreatedDate gt 2019-12-20 ve Status EQ ' Open '"</span><span class="sxs-lookup"><span data-stu-id="9ecbb-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="9ecbb-124">Bu cmdlet öncelikle sayfalamayı destekler ve parametreleri atlar.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="9ecbb-125">Bilet adını belirterek tek bir destek bileti de alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="9ecbb-126">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ecbb-126">EXAMPLES</span></span>

### <span data-ttu-id="9ecbb-127">Örnek 1: ilk 2 bileti alma</span><span class="sxs-lookup"><span data-stu-id="9ecbb-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9ecbb-128">Örnek 2: ilk 2 bileti</span><span class="sxs-lookup"><span data-stu-id="9ecbb-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9ecbb-129">Örnek 3: ada göre destek bileti alma</span><span class="sxs-lookup"><span data-stu-id="9ecbb-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9ecbb-130">Örnek 3: duruma göre filtrelenmiş ilk 2 destek biletlerini alın</span><span class="sxs-lookup"><span data-stu-id="9ecbb-130">Example 3: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="9ecbb-131">Örnek 3: açık durumda olan ve 2019 24 Aralık 'tan sonra oluşturulan tüm destek biletlerini alın.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-131">Example 3: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="9ecbb-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ecbb-132">PARAMETERS</span></span>

### <span data-ttu-id="9ecbb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ecbb-133">-DefaultProfile</span></span>
<span data-ttu-id="9ecbb-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ecbb-135">-Filtre</span><span class="sxs-lookup"><span data-stu-id="9ecbb-135">-Filter</span></span>
<span data-ttu-id="9ecbb-136">Bu cmdlet 'in sonuçlarına uygulanacak filtre.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-136">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ecbb-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ecbb-137">-Name</span></span>
<span data-ttu-id="9ecbb-138">Bu cmdlet 'in aldığı destek anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9ecbb-139">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="9ecbb-139">-IncludeTotalCount</span></span>
<span data-ttu-id="9ecbb-140">Veri kümesindeki toplam nesne sayısını (tamsayı) ve ardından seçilen nesneleri raporlar.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="9ecbb-141">Cmdlet toplam sayısını belirleyemiyorsa, "bilinmeyen toplam sayı" görüntüler.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="9ecbb-142">Tamsayı, toplam sayı değerinin güvenilirliğini belirten bir doğruluk özelliğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="9ecbb-143">0,0 ile 0,0 1,0 arasındaki doğruluk değeri aralığı, cmdlet 'in nesneleri saymadığı anlamına gelir; 1,0, Count 'un tam olduğu ve 0,0 ile 1,0 arasındaki bir değer giderek gittikçe güvenilir bir tahmini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="9ecbb-144">-Atla</span><span class="sxs-lookup"><span data-stu-id="9ecbb-144">-Skip</span></span>
<span data-ttu-id="9ecbb-145">Belirtilen sayıda nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="9ecbb-146">Atlanacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="9ecbb-147">-Önce</span><span class="sxs-lookup"><span data-stu-id="9ecbb-147">-First</span></span>
<span data-ttu-id="9ecbb-148">Yalnızca belirtilen sayıda nesneyi alır.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="9ecbb-149">Alınacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="9ecbb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ecbb-150">CommonParameters</span></span>
<span data-ttu-id="9ecbb-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ecbb-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9ecbb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ecbb-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ecbb-153">INPUTS</span></span>

### <span data-ttu-id="9ecbb-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9ecbb-154">None</span></span>

## <span data-ttu-id="9ecbb-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ecbb-155">OUTPUTS</span></span>

### <span data-ttu-id="9ecbb-156">Microsoft. Azure. Commands. support. model. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="9ecbb-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="9ecbb-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ecbb-157">NOTES</span></span>

## <span data-ttu-id="9ecbb-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ecbb-158">RELATED LINKS</span></span>
