---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5f034253326f551c5b1930f6cf90a80c83ed82f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587437"
---
# <span data-ttu-id="44767-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="44767-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="44767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44767-102">SYNOPSIS</span></span>
<span data-ttu-id="44767-103">Küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="44767-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44767-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44767-104">SYNTAX</span></span>

### <span data-ttu-id="44767-105">BySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44767-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44767-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44767-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44767-107">ByName</span><span class="sxs-lookup"><span data-stu-id="44767-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44767-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="44767-108">DESCRIPTION</span></span>
<span data-ttu-id="44767-109">**Add-AzureRmServiceFabricCluster** , küme kaynağı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="44767-109">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="44767-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44767-110">EXAMPLES</span></span>

### <span data-ttu-id="44767-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44767-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="44767-112">Bu komut, ' myCluster ' kümesi için küme kaynağı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="44767-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="44767-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44767-113">PARAMETERS</span></span>

### <span data-ttu-id="44767-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44767-114">-DefaultProfile</span></span>
<span data-ttu-id="44767-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44767-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44767-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="44767-116">-Name</span></span>
<span data-ttu-id="44767-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="44767-117">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44767-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44767-118">-ResourceGroupName</span></span>
<span data-ttu-id="44767-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44767-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44767-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44767-120">CommonParameters</span></span>
<span data-ttu-id="44767-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44767-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44767-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44767-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44767-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44767-123">INPUTS</span></span>

### <span data-ttu-id="44767-124">System. String</span><span class="sxs-lookup"><span data-stu-id="44767-124">System.String</span></span>

## <span data-ttu-id="44767-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44767-125">OUTPUTS</span></span>

### <span data-ttu-id="44767-126">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster, Microsoft. Azure. Commands. ServiceFabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="44767-126">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="44767-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44767-127">NOTES</span></span>

## <span data-ttu-id="44767-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44767-128">RELATED LINKS</span></span>

