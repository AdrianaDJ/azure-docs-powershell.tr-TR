---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 93ca812f726e036d195e83170153f7b2df4a2352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594216"
---
# <span data-ttu-id="c10d1-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c10d1-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="c10d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c10d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c10d1-103">Power BI çalışma alanı koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="c10d1-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c10d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c10d1-104">SYNTAX</span></span>

### <span data-ttu-id="c10d1-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c10d1-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c10d1-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c10d1-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c10d1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c10d1-107">DESCRIPTION</span></span>
<span data-ttu-id="c10d1-108">**Get-AzureRmPowerBIWorkspaceCollection** cmdlet 'i Azure aboneliğinizdeki veya kaynak GRUBUNDAKI Power BI çalışma alanı koleksiyonlarını veya koleksiyon adını alır.</span><span class="sxs-lookup"><span data-stu-id="c10d1-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="c10d1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c10d1-109">EXAMPLES</span></span>

### <span data-ttu-id="c10d1-110">Örnek 1: kaynak grubundaki tüm çalışma alanı koleksiyonlarını alma</span><span class="sxs-lookup"><span data-stu-id="c10d1-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="c10d1-111">Bu komut, ResourceGroup17 adlı kaynak grubuna ait olan çalışma alanı koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="c10d1-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="c10d1-112">Örnek 2: adını kullanarak çalışma alanı koleksiyonunu alma</span><span class="sxs-lookup"><span data-stu-id="c10d1-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c10d1-113">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="c10d1-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c10d1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c10d1-114">PARAMETERS</span></span>

### <span data-ttu-id="c10d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c10d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="c10d1-116">Bu cmdlet 'in çalışma alanı koleksiyonlarını aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c10d1-116">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="c10d1-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c10d1-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c10d1-118">Bu cmdlet 'in aldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c10d1-118">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c10d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c10d1-119">-DefaultProfile</span></span>
<span data-ttu-id="c10d1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c10d1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c10d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c10d1-121">CommonParameters</span></span>
<span data-ttu-id="c10d1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c10d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c10d1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c10d1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c10d1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c10d1-124">INPUTS</span></span>

## <span data-ttu-id="c10d1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c10d1-125">OUTPUTS</span></span>

### <span data-ttu-id="c10d1-126">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c10d1-126">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="c10d1-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c10d1-127">NOTES</span></span>

## <span data-ttu-id="c10d1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c10d1-128">RELATED LINKS</span></span>

[<span data-ttu-id="c10d1-129">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c10d1-129">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="c10d1-130">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c10d1-130">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


