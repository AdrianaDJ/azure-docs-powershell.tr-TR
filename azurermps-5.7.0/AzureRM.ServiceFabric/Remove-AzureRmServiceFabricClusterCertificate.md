---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: f99d4df206bff962c1cd44a93f1e1ea04aad7740
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587431"
---
# <span data-ttu-id="61d9d-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="61d9d-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="61d9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="61d9d-103">Küme güvenliği için kullanılan küme sertifikasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="61d9d-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61d9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61d9d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61d9d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="61d9d-106">Küme sertifikasını kümeden kaldırmak için, kümede zaten kullanımda olan başka bir sertifika olduğu sürece **Remove-AzureRmServiceFabricClusterCertificate** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="61d9d-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="61d9d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61d9d-107">EXAMPLES</span></span>

### <span data-ttu-id="61d9d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="61d9d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="61d9d-109">Bu komut, küme güvenliği için parmak izi 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A kullanılmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61d9d-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="61d9d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61d9d-110">PARAMETERS</span></span>

### <span data-ttu-id="61d9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d9d-111">-DefaultProfile</span></span>
<span data-ttu-id="61d9d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61d9d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61d9d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="61d9d-113">-Name</span></span>
<span data-ttu-id="61d9d-114">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="61d9d-114">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d9d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d9d-115">-ResourceGroupName</span></span>
<span data-ttu-id="61d9d-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61d9d-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="61d9d-117">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="61d9d-117">-Thumbprint</span></span>
<span data-ttu-id="61d9d-118">Kaldırılacak küme parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="61d9d-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61d9d-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="61d9d-119">-Confirm</span></span>
<span data-ttu-id="61d9d-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61d9d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61d9d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d9d-121">-WhatIf</span></span>
<span data-ttu-id="61d9d-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61d9d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61d9d-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61d9d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61d9d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d9d-124">CommonParameters</span></span>
<span data-ttu-id="61d9d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61d9d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d9d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d9d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d9d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61d9d-127">INPUTS</span></span>

### <span data-ttu-id="61d9d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="61d9d-128">System.String</span></span>

## <span data-ttu-id="61d9d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61d9d-129">OUTPUTS</span></span>

### <span data-ttu-id="61d9d-130">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="61d9d-130">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="61d9d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61d9d-131">NOTES</span></span>

## <span data-ttu-id="61d9d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61d9d-132">RELATED LINKS</span></span>

