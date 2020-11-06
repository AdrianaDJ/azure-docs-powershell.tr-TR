---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7d7fefad86534cd2614312b21bd3ac392050e1b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589397"
---
# <span data-ttu-id="28e86-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="28e86-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="28e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28e86-102">SYNOPSIS</span></span>
<span data-ttu-id="28e86-103">Power BI çalışma alanı koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="28e86-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28e86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28e86-104">SYNTAX</span></span>

### <span data-ttu-id="28e86-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="28e86-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28e86-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28e86-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28e86-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="28e86-107">DESCRIPTION</span></span>
<span data-ttu-id="28e86-108">**Get-AzureRmPowerBIWorkspaceCollection** cmdlet 'i Azure aboneliğinizdeki veya kaynak GRUBUNDAKI Power BI çalışma alanı koleksiyonlarını veya koleksiyon adını alır.</span><span class="sxs-lookup"><span data-stu-id="28e86-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="28e86-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28e86-109">EXAMPLES</span></span>

### <span data-ttu-id="28e86-110">Örnek 1: kaynak grubundaki tüm çalışma alanı koleksiyonlarını alma</span><span class="sxs-lookup"><span data-stu-id="28e86-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="28e86-111">Bu komut, ResourceGroup17 adlı kaynak grubuna ait olan çalışma alanı koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="28e86-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="28e86-112">Örnek 2: adını kullanarak çalışma alanı koleksiyonunu alma</span><span class="sxs-lookup"><span data-stu-id="28e86-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="28e86-113">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="28e86-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="28e86-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28e86-114">PARAMETERS</span></span>

### <span data-ttu-id="28e86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e86-115">-DefaultProfile</span></span>
<span data-ttu-id="28e86-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="28e86-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28e86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28e86-117">-ResourceGroupName</span></span>
<span data-ttu-id="28e86-118">Bu cmdlet 'in çalışma alanı koleksiyonlarını aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28e86-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28e86-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="28e86-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="28e86-120">Bu cmdlet 'in aldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28e86-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28e86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e86-121">CommonParameters</span></span>
<span data-ttu-id="28e86-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28e86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e86-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28e86-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e86-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28e86-124">INPUTS</span></span>

### <span data-ttu-id="28e86-125">System. String</span><span class="sxs-lookup"><span data-stu-id="28e86-125">System.String</span></span>

## <span data-ttu-id="28e86-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28e86-126">OUTPUTS</span></span>

### <span data-ttu-id="28e86-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="28e86-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="28e86-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28e86-128">NOTES</span></span>

## <span data-ttu-id="28e86-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28e86-129">RELATED LINKS</span></span>

[<span data-ttu-id="28e86-130">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="28e86-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="28e86-131">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="28e86-131">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


