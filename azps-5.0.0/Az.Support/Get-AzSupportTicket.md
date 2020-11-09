---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324865"
---
# <span data-ttu-id="5f427-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5f427-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="5f427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f427-102">SYNOPSIS</span></span>
<span data-ttu-id="5f427-103">Destek biletlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="5f427-103">Get support tickets.</span></span>

## <span data-ttu-id="5f427-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f427-104">SYNTAX</span></span>

### <span data-ttu-id="5f427-105">ListParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f427-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5f427-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f427-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5f427-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f427-107">DESCRIPTION</span></span>
<span data-ttu-id="5f427-108">Destek biletleri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="5f427-108">Gets the list of support tickets.</span></span> <span data-ttu-id="5f427-109">Herhangi bir parametre belirtmezseniz tüm destek biletlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5f427-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="5f427-110">Ayrıca, filtre parametresini kullanarak destek biletlerini duruma veya CreatedDate 'e göre de filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5f427-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="5f427-111">Burada, belirleyebileceğiniz filtre değerlerine örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5f427-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="5f427-112">Vurgu</span><span class="sxs-lookup"><span data-stu-id="5f427-112">Scenario</span></span>                                                         | <span data-ttu-id="5f427-113">Filtreleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5f427-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="5f427-114">Açık durumda olan anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="5f427-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="5f427-115">"Durum EQ ' Aç '"</span><span class="sxs-lookup"><span data-stu-id="5f427-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="5f427-116">Kapatma durumundaki anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="5f427-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="5f427-117">"Durum EQ ' kapandı '"</span><span class="sxs-lookup"><span data-stu-id="5f427-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="5f427-118">20 ' nin üstünde veya altında oluşturulmuş anahtarları 2019</span><span class="sxs-lookup"><span data-stu-id="5f427-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="5f427-119">"CreatedDate Ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="5f427-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="5f427-120">20 ' den sonra oluşturulmuş anahtarları alın, 2019</span><span class="sxs-lookup"><span data-stu-id="5f427-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="5f427-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="5f427-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="5f427-122">20 2019 ' den sonra oluşturulan anahtarları alır; açık durumda.</span><span class="sxs-lookup"><span data-stu-id="5f427-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="5f427-123">"CreatedDate gt 2019-12-20 ve Status EQ ' Open '"</span><span class="sxs-lookup"><span data-stu-id="5f427-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="5f427-124">Bu cmdlet öncelikle sayfalamayı destekler ve parametreleri atlar.</span><span class="sxs-lookup"><span data-stu-id="5f427-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="5f427-125">Bilet adını belirterek tek bir destek bileti de alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5f427-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="5f427-126">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f427-126">EXAMPLES</span></span>

### <span data-ttu-id="5f427-127">Örnek 1: ilk 2 bileti alma</span><span class="sxs-lookup"><span data-stu-id="5f427-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5f427-128">Örnek 2: ilk 2 bileti</span><span class="sxs-lookup"><span data-stu-id="5f427-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5f427-129">Örnek 3: ada göre destek bileti alma</span><span class="sxs-lookup"><span data-stu-id="5f427-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5f427-130">Örnek 4: duruma göre filtrelenmiş ilk 2 destek biletlerini alın</span><span class="sxs-lookup"><span data-stu-id="5f427-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="5f427-131">Örnek 5: açık durumda olan ve 2019 24 Aralık 'tan sonra oluşturulan tüm destek biletlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="5f427-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="5f427-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f427-132">PARAMETERS</span></span>

### <span data-ttu-id="5f427-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f427-133">-DefaultProfile</span></span>
<span data-ttu-id="5f427-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f427-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f427-135">-Filtre</span><span class="sxs-lookup"><span data-stu-id="5f427-135">-Filter</span></span>
<span data-ttu-id="5f427-136">Bu cmdlet 'in sonuçlarına uygulanacak filtre.</span><span class="sxs-lookup"><span data-stu-id="5f427-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="5f427-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f427-137">-Name</span></span>
<span data-ttu-id="5f427-138">Bu cmdlet 'in aldığı destek anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="5f427-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f427-139">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="5f427-139">-IncludeTotalCount</span></span>
<span data-ttu-id="5f427-140">Veri kümesindeki toplam nesne sayısını (tamsayı) ve ardından seçilen nesneleri raporlar.</span><span class="sxs-lookup"><span data-stu-id="5f427-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="5f427-141">Cmdlet toplam sayısını belirleyemiyorsa, "bilinmeyen toplam sayı" görüntüler.</span><span class="sxs-lookup"><span data-stu-id="5f427-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="5f427-142">Tamsayı, toplam sayı değerinin güvenilirliğini belirten bir doğruluk özelliğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="5f427-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="5f427-143">0,0 ile 0,0 1,0 arasındaki doğruluk değeri aralığı, cmdlet 'in nesneleri saymadığı anlamına gelir; 1,0, Count 'un tam olduğu ve 0,0 ile 1,0 arasındaki bir değer giderek gittikçe güvenilir bir tahmini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="5f427-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="5f427-144">-Atla</span><span class="sxs-lookup"><span data-stu-id="5f427-144">-Skip</span></span>
<span data-ttu-id="5f427-145">Belirtilen sayıda nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="5f427-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="5f427-146">Atlanacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="5f427-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="5f427-147">-Önce</span><span class="sxs-lookup"><span data-stu-id="5f427-147">-First</span></span>
<span data-ttu-id="5f427-148">Yalnızca belirtilen sayıda nesneyi alır.</span><span class="sxs-lookup"><span data-stu-id="5f427-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="5f427-149">Alınacak nesne sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="5f427-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="5f427-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f427-150">CommonParameters</span></span>
<span data-ttu-id="5f427-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f427-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f427-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f427-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f427-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f427-153">INPUTS</span></span>

### <span data-ttu-id="5f427-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5f427-154">None</span></span>

## <span data-ttu-id="5f427-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f427-155">OUTPUTS</span></span>

### <span data-ttu-id="5f427-156">Microsoft. Azure. Commands. support. model. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="5f427-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="5f427-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f427-157">NOTES</span></span>

## <span data-ttu-id="5f427-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f427-158">RELATED LINKS</span></span>
