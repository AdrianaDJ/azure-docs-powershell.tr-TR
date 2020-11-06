---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593121"
---
# <span data-ttu-id="e1f48-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1f48-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="e1f48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f48-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f48-103">Uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e1f48-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1f48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1f48-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1f48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1f48-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f48-106">**Remove-AzureRmAlertRule** cmdlet 'i bir uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e1f48-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="e1f48-107">Uyarı kuralının adını ve atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e1f48-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="e1f48-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1f48-108">EXAMPLES</span></span>

### <span data-ttu-id="e1f48-109">Örnek 1: uyarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e1f48-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="e1f48-110">Bu komut, varsayılan-Web-Merkezileştirmeli ABD 'de myalert-7DA, 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e1f48-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="e1f48-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1f48-111">PARAMETERS</span></span>

### <span data-ttu-id="e1f48-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1f48-112">-Name</span></span>
<span data-ttu-id="e1f48-113">Kaldırılacak uyarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1f48-113">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f48-114">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1f48-114">-ResourceGroup</span></span>
<span data-ttu-id="e1f48-115">Uyarı kuralının kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1f48-115">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f48-116">-DefaultProfile</span></span>
<span data-ttu-id="e1f48-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1f48-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f48-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f48-118">CommonParameters</span></span>
<span data-ttu-id="e1f48-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1f48-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f48-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f48-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f48-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1f48-121">INPUTS</span></span>

## <span data-ttu-id="e1f48-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1f48-122">OUTPUTS</span></span>

### <span data-ttu-id="e1f48-123">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="e1f48-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="e1f48-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1f48-124">NOTES</span></span>

## <span data-ttu-id="e1f48-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1f48-125">RELATED LINKS</span></span>

[<span data-ttu-id="e1f48-126">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1f48-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="e1f48-127">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1f48-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e1f48-128">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1f48-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="e1f48-129">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e1f48-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="e1f48-130">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1f48-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


