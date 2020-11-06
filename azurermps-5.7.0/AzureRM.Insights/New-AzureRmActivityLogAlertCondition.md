---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: d9309f2de88dc87368b510cdf6f1062d03c7f709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590479"
---
# <span data-ttu-id="9d2b6-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9d2b6-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="9d2b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="9d2b6-103">Bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d2b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d2b6-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d2b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d2b6-105">DESCRIPTION</span></span>
<span data-ttu-id="9d2b6-106">**Yeni-Azurermacmaclogalertcondition** cmdlet 'i bellekte yeni etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="9d2b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d2b6-107">EXAMPLES</span></span>

### <span data-ttu-id="9d2b6-108">Örnek 1: bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="9d2b6-109">Bu komut, bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-109">This command creates a new activity log alert condition object in memory.</span></span>

<span data-ttu-id="9d2b6-110">**Not** : Bu cmdlet, parametre olarak geçirilen bu nesnelerden en az biriyle Set-AzureRmActivityLogAlert ile kullanıldığında, alanı "Category" değerine eşit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="9d2b6-111">Aksi takdirde, arka uç 400 (BadRequest) ile yanıt verir.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="9d2b6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d2b6-112">PARAMETERS</span></span>

### <span data-ttu-id="9d2b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d2b6-113">-DefaultProfile</span></span>
<span data-ttu-id="9d2b6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9d2b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d2b6-115">-Eşittir</span><span class="sxs-lookup"><span data-stu-id="9d2b6-115">-Equal</span></span>
<span data-ttu-id="9d2b6-116">Yaprak koşulunun eşittir özelliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d2b6-117">-Alan</span><span class="sxs-lookup"><span data-stu-id="9d2b6-117">-Field</span></span>
<span data-ttu-id="9d2b6-118">Koşul için alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-118">Specifies the field for the condition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d2b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d2b6-119">CommonParameters</span></span>
<span data-ttu-id="9d2b6-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d2b6-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d2b6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d2b6-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d2b6-122">INPUTS</span></span>

### <span data-ttu-id="9d2b6-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9d2b6-123">None</span></span>
<span data-ttu-id="9d2b6-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9d2b6-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d2b6-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d2b6-125">OUTPUTS</span></span>

### <span data-ttu-id="9d2b6-126">Microsoft. Azure. Management. Monitor. Management. modeller. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="9d2b6-126">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="9d2b6-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d2b6-127">NOTES</span></span>

## <span data-ttu-id="9d2b6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d2b6-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d2b6-129">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d2b6-129">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9d2b6-130">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d2b6-130">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9d2b6-131">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d2b6-131">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9d2b6-132">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d2b6-132">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9d2b6-133">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d2b6-133">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9d2b6-134">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9d2b6-134">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
