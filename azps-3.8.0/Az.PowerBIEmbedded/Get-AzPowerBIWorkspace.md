---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096146"
---
# <span data-ttu-id="f94d0-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="f94d0-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="f94d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f94d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f94d0-103">Power BI çalışma alanı koleksiyonundaki çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f94d0-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="f94d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f94d0-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f94d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f94d0-105">DESCRIPTION</span></span>
<span data-ttu-id="f94d0-106">**Get-AzPowerBIWorkspace** cmdlet 'ı Power BI çalışma alanı koleksiyonundaki çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f94d0-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="f94d0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f94d0-107">EXAMPLES</span></span>

### <span data-ttu-id="f94d0-108">Örnek 1: çalışma alanı koleksiyonunun çalışma alanlarını alma</span><span class="sxs-lookup"><span data-stu-id="f94d0-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="f94d0-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonuna ait olan çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f94d0-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="f94d0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f94d0-110">PARAMETERS</span></span>

### <span data-ttu-id="f94d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94d0-111">-DefaultProfile</span></span>
<span data-ttu-id="f94d0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f94d0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f94d0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94d0-113">-ResourceGroupName</span></span>
<span data-ttu-id="f94d0-114">Çalışma alanı koleksiyonunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f94d0-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="f94d0-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="f94d0-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="f94d0-116">Bu cmdlet 'in çalışma alanlarını aldığı çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f94d0-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="f94d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94d0-117">CommonParameters</span></span>
<span data-ttu-id="f94d0-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f94d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94d0-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f94d0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94d0-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f94d0-120">INPUTS</span></span>

### <span data-ttu-id="f94d0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f94d0-121">System.String</span></span>

## <span data-ttu-id="f94d0-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f94d0-122">OUTPUTS</span></span>

### <span data-ttu-id="f94d0-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f94d0-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="f94d0-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f94d0-124">NOTES</span></span>

## <span data-ttu-id="f94d0-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f94d0-125">RELATED LINKS</span></span>

[<span data-ttu-id="f94d0-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f94d0-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


