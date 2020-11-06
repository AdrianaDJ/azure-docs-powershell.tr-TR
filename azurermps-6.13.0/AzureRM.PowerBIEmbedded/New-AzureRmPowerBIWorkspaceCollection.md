---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7ed4af8c6d5443c3cdc7c8ae395ecc66d0a927e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588415"
---
# <span data-ttu-id="1ceae-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1ceae-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="1ceae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ceae-102">SYNOPSIS</span></span>
<span data-ttu-id="1ceae-103">Power BI çalışma alanı koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ceae-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ceae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ceae-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ceae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ceae-105">DESCRIPTION</span></span>
<span data-ttu-id="1ceae-106">**New-AzureRmPowerBIWorkspaceCollection** cmdlet 'i, belirtilen kaynak grubunda ve konumunda Azure aboneliğiniz Için BIR Power BI çalışma alanı koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ceae-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="1ceae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ceae-107">EXAMPLES</span></span>

### <span data-ttu-id="1ceae-108">Örnek 1: çalışma alanı koleksiyonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ceae-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="1ceae-109">Bu komut belirtilen konumda belirtilen kaynak grubunda WCN11 adlı bir çalışma alanı koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ceae-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="1ceae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ceae-110">PARAMETERS</span></span>

### <span data-ttu-id="1ceae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ceae-111">-DefaultProfile</span></span>
<span data-ttu-id="1ceae-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1ceae-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ceae-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="1ceae-113">-Location</span></span>
<span data-ttu-id="1ceae-114">Bu cmdlet 'in bir çalışma alanı koleksiyonu oluşturduğu Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ceae-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ceae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ceae-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ceae-116">Bu cmdlet 'in çalışma alanı koleksiyonu oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ceae-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="1ceae-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1ceae-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="1ceae-118">Power BI çalışma alanı koleksiyonu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ceae-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="1ceae-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ceae-119">-Confirm</span></span>
<span data-ttu-id="1ceae-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ceae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ceae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ceae-121">-WhatIf</span></span>
<span data-ttu-id="1ceae-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ceae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ceae-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ceae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ceae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ceae-124">CommonParameters</span></span>
<span data-ttu-id="1ceae-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ceae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ceae-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ceae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ceae-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ceae-127">INPUTS</span></span>

### <span data-ttu-id="1ceae-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1ceae-128">System.String</span></span>

## <span data-ttu-id="1ceae-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ceae-129">OUTPUTS</span></span>

### <span data-ttu-id="1ceae-130">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1ceae-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="1ceae-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ceae-131">NOTES</span></span>

## <span data-ttu-id="1ceae-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ceae-132">RELATED LINKS</span></span>

[<span data-ttu-id="1ceae-133">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1ceae-133">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="1ceae-134">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1ceae-134">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


