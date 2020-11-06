---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 93240fe3deddbe5b6f8fb20d644a0e685cfdda11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592730"
---
# <span data-ttu-id="19bd9-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="19bd9-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="19bd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="19bd9-103">Küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="19bd9-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19bd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19bd9-104">SYNTAX</span></span>

### <span data-ttu-id="19bd9-105">BySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19bd9-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19bd9-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="19bd9-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19bd9-107">ByName</span><span class="sxs-lookup"><span data-stu-id="19bd9-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19bd9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="19bd9-108">DESCRIPTION</span></span>
<span data-ttu-id="19bd9-109">**Get-AzureRmServiceFabricCluster** , küme kaynağı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="19bd9-109">The **Get-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="19bd9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19bd9-110">EXAMPLES</span></span>

### <span data-ttu-id="19bd9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19bd9-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="19bd9-112">Bu komut, ' myCluster ' kümesi için küme kaynağı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="19bd9-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="19bd9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19bd9-113">PARAMETERS</span></span>

### <span data-ttu-id="19bd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bd9-114">-DefaultProfile</span></span>
<span data-ttu-id="19bd9-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19bd9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19bd9-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="19bd9-116">-Name</span></span>
<span data-ttu-id="19bd9-117">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="19bd9-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19bd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="19bd9-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19bd9-119">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bd9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bd9-120">CommonParameters</span></span>
<span data-ttu-id="19bd9-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19bd9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bd9-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19bd9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bd9-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19bd9-123">INPUTS</span></span>

### <span data-ttu-id="19bd9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="19bd9-124">System.String</span></span>

## <span data-ttu-id="19bd9-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19bd9-125">OUTPUTS</span></span>

### <span data-ttu-id="19bd9-126">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="19bd9-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="19bd9-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19bd9-127">NOTES</span></span>

## <span data-ttu-id="19bd9-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19bd9-128">RELATED LINKS</span></span>
