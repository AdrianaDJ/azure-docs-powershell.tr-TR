---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 3c8dda7d7b84ae4ee7017c88e211b2ab5db46360
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937277"
---
# <span data-ttu-id="47438-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="47438-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="47438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47438-102">SYNOPSIS</span></span>
<span data-ttu-id="47438-103">Günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47438-103">Removes a log profile.</span></span>

## <span data-ttu-id="47438-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47438-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47438-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47438-105">DESCRIPTION</span></span>
<span data-ttu-id="47438-106">**Remove-AzLogProfile** cmdlet 'i, günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47438-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="47438-107">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="47438-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="47438-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47438-108">EXAMPLES</span></span>

## <span data-ttu-id="47438-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47438-109">PARAMETERS</span></span>

### <span data-ttu-id="47438-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47438-110">-DefaultProfile</span></span>
<span data-ttu-id="47438-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="47438-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47438-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="47438-112">-Name</span></span>
<span data-ttu-id="47438-113">Kaldırılacak günlük profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47438-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="47438-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="47438-114">-PassThru</span></span>
<span data-ttu-id="47438-115">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="47438-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="47438-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="47438-116">-Confirm</span></span>
<span data-ttu-id="47438-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47438-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47438-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47438-118">-WhatIf</span></span>
<span data-ttu-id="47438-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47438-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47438-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47438-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47438-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47438-121">CommonParameters</span></span>
<span data-ttu-id="47438-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47438-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47438-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="47438-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47438-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47438-124">INPUTS</span></span>

### <span data-ttu-id="47438-125">System. String</span><span class="sxs-lookup"><span data-stu-id="47438-125">System.String</span></span>

## <span data-ttu-id="47438-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47438-126">OUTPUTS</span></span>

### <span data-ttu-id="47438-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="47438-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="47438-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47438-128">NOTES</span></span>

## <span data-ttu-id="47438-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47438-129">RELATED LINKS</span></span>

[<span data-ttu-id="47438-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="47438-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="47438-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="47438-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


