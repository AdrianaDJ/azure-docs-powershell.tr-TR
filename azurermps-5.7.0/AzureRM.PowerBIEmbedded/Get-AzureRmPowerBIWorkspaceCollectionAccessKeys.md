---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 11c1e3c19a6f5767fcfe1120cfa3561a73885f5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588123"
---
# <span data-ttu-id="da8b7-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="da8b7-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="da8b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="da8b7-103">Power BI çalışma alanı koleksiyonuyla ilişkili geçerli erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="da8b7-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da8b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da8b7-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da8b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da8b7-105">DESCRIPTION</span></span>
<span data-ttu-id="da8b7-106">**Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet 'ı, Power BI çalışma alanı koleksiyonuyla ilişkili geçerli erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="da8b7-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="da8b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da8b7-107">EXAMPLES</span></span>

### <span data-ttu-id="da8b7-108">Örnek 1: erişim tuşlarını alın</span><span class="sxs-lookup"><span data-stu-id="da8b7-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="da8b7-109">Bu komut, belirtilen kaynak grubundaki WCN11 adındaki çalışma alanı koleksiyonu için erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="da8b7-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="da8b7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da8b7-110">PARAMETERS</span></span>

### <span data-ttu-id="da8b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8b7-111">-DefaultProfile</span></span>
<span data-ttu-id="da8b7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="da8b7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da8b7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da8b7-113">-ResourceGroupName</span></span>
<span data-ttu-id="da8b7-114">Koleksiyonun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da8b7-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="da8b7-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="da8b7-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="da8b7-116">Bu cmdlet 'in üzerinde çalıştırıldığı Power BI çalışma alanı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da8b7-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="da8b7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8b7-117">CommonParameters</span></span>
<span data-ttu-id="da8b7-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da8b7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8b7-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da8b7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8b7-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da8b7-120">INPUTS</span></span>

### <span data-ttu-id="da8b7-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="da8b7-121">None</span></span>
<span data-ttu-id="da8b7-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="da8b7-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da8b7-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da8b7-123">OUTPUTS</span></span>

### <span data-ttu-id="da8b7-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. model. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="da8b7-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="da8b7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da8b7-125">NOTES</span></span>

## <span data-ttu-id="da8b7-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da8b7-126">RELATED LINKS</span></span>

[<span data-ttu-id="da8b7-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="da8b7-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


