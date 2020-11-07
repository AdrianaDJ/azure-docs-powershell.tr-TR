---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: ddc11d8bd7eaa6a844d921aacb4870df1566d2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932165"
---
# <span data-ttu-id="0c6b7-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="0c6b7-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="0c6b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6b7-103">Uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-103">Removes an alert rule.</span></span>

## <span data-ttu-id="0c6b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c6b7-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c6b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c6b7-105">DESCRIPTION</span></span>
<span data-ttu-id="0c6b7-106">**Remove-AzAlertRule** cmdlet 'i bir uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="0c6b7-107">Uyarı kuralının adını ve atandığı kaynak grubunu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="0c6b7-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0c6b7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c6b7-109">EXAMPLES</span></span>

### <span data-ttu-id="0c6b7-110">Örnek 1: uyarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0c6b7-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="0c6b7-111">Bu komut, varsayılan-Web-Merkezileştirmeli ABD 'de myalert-7DA, 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="0c6b7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c6b7-112">PARAMETERS</span></span>

### <span data-ttu-id="0c6b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6b7-113">-DefaultProfile</span></span>
<span data-ttu-id="0c6b7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0c6b7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c6b7-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c6b7-115">-Name</span></span>
<span data-ttu-id="0c6b7-116">Kaldırılacak uyarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="0c6b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="0c6b7-118">Uyarı kuralının kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b7-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c6b7-119">-Confirm</span></span>
<span data-ttu-id="0c6b7-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6b7-121">-WhatIf</span></span>
<span data-ttu-id="0c6b7-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c6b7-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c6b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6b7-124">CommonParameters</span></span>
<span data-ttu-id="0c6b7-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6b7-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c6b7-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6b7-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c6b7-127">INPUTS</span></span>

### <span data-ttu-id="0c6b7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0c6b7-128">System.String</span></span>

## <span data-ttu-id="0c6b7-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c6b7-129">OUTPUTS</span></span>

### <span data-ttu-id="0c6b7-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0c6b7-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0c6b7-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c6b7-131">NOTES</span></span>

## <span data-ttu-id="0c6b7-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c6b7-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c6b7-133">Add-Azmetrik ıalertrule</span><span class="sxs-lookup"><span data-stu-id="0c6b7-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="0c6b7-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0c6b7-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="0c6b7-135">Get-Azalera</span><span class="sxs-lookup"><span data-stu-id="0c6b7-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="0c6b7-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="0c6b7-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


