---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: eaa7cfa9f58bb9bb5affa7a035d194910bcf0006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588925"
---
# <span data-ttu-id="b5e33-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5e33-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="b5e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5e33-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e33-103">Uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5e33-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5e33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5e33-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5e33-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5e33-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e33-106">**Remove-AzureRmAlertRule** cmdlet 'i bir uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5e33-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="b5e33-107">Uyarı kuralının adını ve atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5e33-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

<span data-ttu-id="b5e33-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="b5e33-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b5e33-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5e33-109">EXAMPLES</span></span>

### <span data-ttu-id="b5e33-110">Örnek 1: uyarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b5e33-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="b5e33-111">Bu komut, varsayılan-Web-Merkezileştirmeli ABD 'de myalert-7DA, 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5e33-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="b5e33-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5e33-112">PARAMETERS</span></span>

### <span data-ttu-id="b5e33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e33-113">-DefaultProfile</span></span>
<span data-ttu-id="b5e33-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b5e33-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5e33-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5e33-115">-Name</span></span>
<span data-ttu-id="b5e33-116">Kaldırılacak uyarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e33-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="b5e33-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e33-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5e33-118">Uyarı kuralının kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e33-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e33-119">CommonParameters</span></span>
<span data-ttu-id="b5e33-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5e33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e33-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e33-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e33-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5e33-122">INPUTS</span></span>

### <span data-ttu-id="b5e33-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b5e33-123">None</span></span>
<span data-ttu-id="b5e33-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b5e33-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5e33-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5e33-125">OUTPUTS</span></span>

### <span data-ttu-id="b5e33-126">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b5e33-126">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b5e33-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5e33-127">NOTES</span></span>

## <span data-ttu-id="b5e33-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5e33-128">RELATED LINKS</span></span>

[<span data-ttu-id="b5e33-129">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5e33-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b5e33-130">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5e33-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b5e33-131">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b5e33-131">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="b5e33-132">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5e33-132">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


