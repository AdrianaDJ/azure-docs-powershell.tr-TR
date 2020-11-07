---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 19b1d1b0da719167d53739a8c92a97121656aa9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932807"
---
# <span data-ttu-id="540ab-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="540ab-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="540ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="540ab-102">SYNOPSIS</span></span>
<span data-ttu-id="540ab-103">Power BI çalışma alanı koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="540ab-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="540ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="540ab-104">SYNTAX</span></span>

### <span data-ttu-id="540ab-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="540ab-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="540ab-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="540ab-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="540ab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="540ab-107">DESCRIPTION</span></span>
<span data-ttu-id="540ab-108">**Get-AzPowerBIWorkspaceCollection** cmdlet 'i Azure aboneliğinizdeki veya kaynak GRUBUNDAKI Power BI çalışma alanı koleksiyonlarını veya koleksiyon adını alır.</span><span class="sxs-lookup"><span data-stu-id="540ab-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="540ab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="540ab-109">EXAMPLES</span></span>

### <span data-ttu-id="540ab-110">Örnek 1: kaynak grubundaki tüm çalışma alanı koleksiyonlarını alma</span><span class="sxs-lookup"><span data-stu-id="540ab-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="540ab-111">Bu komut, ResourceGroup17 adlı kaynak grubuna ait olan çalışma alanı koleksiyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="540ab-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="540ab-112">Örnek 2: adını kullanarak çalışma alanı koleksiyonunu alma</span><span class="sxs-lookup"><span data-stu-id="540ab-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="540ab-113">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="540ab-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="540ab-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="540ab-114">PARAMETERS</span></span>

### <span data-ttu-id="540ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540ab-115">-DefaultProfile</span></span>
<span data-ttu-id="540ab-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="540ab-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="540ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="540ab-118">Bu cmdlet 'in çalışma alanı koleksiyonlarını aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="540ab-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="540ab-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="540ab-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="540ab-120">Bu cmdlet 'in aldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="540ab-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="540ab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540ab-121">CommonParameters</span></span>
<span data-ttu-id="540ab-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="540ab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540ab-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="540ab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540ab-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="540ab-124">INPUTS</span></span>

### <span data-ttu-id="540ab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="540ab-125">System.String</span></span>

## <span data-ttu-id="540ab-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="540ab-126">OUTPUTS</span></span>

### <span data-ttu-id="540ab-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="540ab-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="540ab-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="540ab-128">NOTES</span></span>

## <span data-ttu-id="540ab-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="540ab-129">RELATED LINKS</span></span>

[<span data-ttu-id="540ab-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="540ab-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="540ab-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="540ab-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


