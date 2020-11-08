---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267437"
---
# <span data-ttu-id="03464-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="03464-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="03464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03464-102">SYNOPSIS</span></span>
<span data-ttu-id="03464-103">Power BI çalışma alanı koleksiyonundaki çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="03464-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="03464-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03464-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03464-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03464-105">DESCRIPTION</span></span>
<span data-ttu-id="03464-106">**Get-AzPowerBIWorkspace** cmdlet 'ı Power BI çalışma alanı koleksiyonundaki çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="03464-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="03464-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03464-107">EXAMPLES</span></span>

### <span data-ttu-id="03464-108">Örnek 1: çalışma alanı koleksiyonunun çalışma alanlarını alma</span><span class="sxs-lookup"><span data-stu-id="03464-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="03464-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonuna ait olan çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="03464-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="03464-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03464-110">PARAMETERS</span></span>

### <span data-ttu-id="03464-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03464-111">-DefaultProfile</span></span>
<span data-ttu-id="03464-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="03464-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03464-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03464-113">-ResourceGroupName</span></span>
<span data-ttu-id="03464-114">Çalışma alanı koleksiyonunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03464-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="03464-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="03464-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="03464-116">Bu cmdlet 'in çalışma alanlarını aldığı çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03464-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="03464-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03464-117">CommonParameters</span></span>
<span data-ttu-id="03464-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03464-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03464-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03464-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03464-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03464-120">INPUTS</span></span>

### <span data-ttu-id="03464-121">System. String</span><span class="sxs-lookup"><span data-stu-id="03464-121">System.String</span></span>

## <span data-ttu-id="03464-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03464-122">OUTPUTS</span></span>

### <span data-ttu-id="03464-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="03464-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="03464-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03464-124">NOTES</span></span>

## <span data-ttu-id="03464-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03464-125">RELATED LINKS</span></span>

[<span data-ttu-id="03464-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="03464-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


