---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594564"
---
# <span data-ttu-id="dda07-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="dda07-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="dda07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dda07-102">SYNOPSIS</span></span>
<span data-ttu-id="dda07-103">Küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="dda07-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dda07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dda07-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dda07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dda07-105">DESCRIPTION</span></span>
<span data-ttu-id="dda07-106">**Add-AzureRmServiceFabricCluster** , küme kaynağı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dda07-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="dda07-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dda07-107">EXAMPLES</span></span>

### <span data-ttu-id="dda07-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dda07-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="dda07-109">Bu komut, ' myCluster ' kümesi için küme kaynağı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dda07-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="dda07-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dda07-110">PARAMETERS</span></span>

### <span data-ttu-id="dda07-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="dda07-111">-Name</span></span>
<span data-ttu-id="dda07-112">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="dda07-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda07-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda07-113">-ResourceGroupName</span></span>
<span data-ttu-id="dda07-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dda07-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda07-115">-DefaultProfile</span></span>
<span data-ttu-id="dda07-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dda07-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dda07-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda07-117">CommonParameters</span></span>
<span data-ttu-id="dda07-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dda07-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda07-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda07-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda07-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dda07-120">INPUTS</span></span>

### <span data-ttu-id="dda07-121">System. String</span><span class="sxs-lookup"><span data-stu-id="dda07-121">System.String</span></span>

## <span data-ttu-id="dda07-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dda07-122">OUTPUTS</span></span>

### <span data-ttu-id="dda07-123">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster, Microsoft. Azure. Commands. ServiceFabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dda07-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dda07-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dda07-124">NOTES</span></span>

## <span data-ttu-id="dda07-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dda07-125">RELATED LINKS</span></span>

