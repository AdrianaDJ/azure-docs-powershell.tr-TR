---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c8e6f54b5bd4deeb4ef24559298306880740c6d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097815"
---
# <span data-ttu-id="9bc44-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9bc44-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="9bc44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc44-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc44-103">Power BI çalışma alanı koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9bc44-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="9bc44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bc44-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bc44-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bc44-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc44-106">**Remove-AzPowerBIWorkspaceCollection** cmdlet 'ı, Azure aboneliğinizden ve kaynak Grupunuzdan Power BI çalışma alanı koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9bc44-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="9bc44-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bc44-107">EXAMPLES</span></span>

### <span data-ttu-id="9bc44-108">Örnek 1: çalışma alanı koleksiyonunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="9bc44-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="9bc44-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9bc44-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="9bc44-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bc44-110">PARAMETERS</span></span>

### <span data-ttu-id="9bc44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc44-111">-DefaultProfile</span></span>
<span data-ttu-id="9bc44-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9bc44-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bc44-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc44-113">-ResourceGroupName</span></span>
<span data-ttu-id="9bc44-114">Bu cmdlet 'in çalışma alanı koleksiyonunu kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bc44-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc44-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="9bc44-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="9bc44-116">Bu cmdlet 'in kaldırıldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bc44-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc44-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="9bc44-117">-Confirm</span></span>
<span data-ttu-id="9bc44-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9bc44-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc44-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc44-119">-WhatIf</span></span>
<span data-ttu-id="9bc44-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9bc44-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bc44-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9bc44-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc44-122">CommonParameters</span></span>
<span data-ttu-id="9bc44-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bc44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc44-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc44-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc44-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bc44-125">INPUTS</span></span>

### <span data-ttu-id="9bc44-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9bc44-126">System.String</span></span>

## <span data-ttu-id="9bc44-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bc44-127">OUTPUTS</span></span>

### <span data-ttu-id="9bc44-128">System. void</span><span class="sxs-lookup"><span data-stu-id="9bc44-128">System.Void</span></span>

## <span data-ttu-id="9bc44-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bc44-129">NOTES</span></span>

## <span data-ttu-id="9bc44-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bc44-130">RELATED LINKS</span></span>

[<span data-ttu-id="9bc44-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9bc44-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="9bc44-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9bc44-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

