---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c94486e33ac39bff9d378840a6ab0ad041fa998e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588128"
---
# <span data-ttu-id="1d21d-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d21d-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="1d21d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d21d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d21d-103">Power BI çalışma alanı koleksiyonundaki çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="1d21d-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d21d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d21d-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d21d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d21d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d21d-106">**Get-Azurermpowerbibıworkspace** cmdlet 'ı Power BI çalışma alanı koleksiyonundaki çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="1d21d-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="1d21d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d21d-107">EXAMPLES</span></span>

### <span data-ttu-id="1d21d-108">Örnek 1: çalışma alanı koleksiyonunun çalışma alanlarını alma</span><span class="sxs-lookup"><span data-stu-id="1d21d-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="1d21d-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonuna ait olan çalışma alanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="1d21d-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="1d21d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d21d-110">PARAMETERS</span></span>

### <span data-ttu-id="1d21d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d21d-111">-DefaultProfile</span></span>
<span data-ttu-id="1d21d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1d21d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d21d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d21d-113">-ResourceGroupName</span></span>
<span data-ttu-id="1d21d-114">Çalışma alanı koleksiyonunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d21d-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d21d-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1d21d-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="1d21d-116">Bu cmdlet 'in çalışma alanlarını aldığı çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d21d-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d21d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d21d-117">CommonParameters</span></span>
<span data-ttu-id="1d21d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d21d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d21d-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d21d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d21d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d21d-120">INPUTS</span></span>

### <span data-ttu-id="1d21d-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1d21d-121">None</span></span>
<span data-ttu-id="1d21d-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1d21d-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d21d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d21d-123">OUTPUTS</span></span>

### <span data-ttu-id="1d21d-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d21d-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="1d21d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d21d-125">NOTES</span></span>

## <span data-ttu-id="1d21d-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d21d-126">RELATED LINKS</span></span>

[<span data-ttu-id="1d21d-127">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1d21d-127">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


