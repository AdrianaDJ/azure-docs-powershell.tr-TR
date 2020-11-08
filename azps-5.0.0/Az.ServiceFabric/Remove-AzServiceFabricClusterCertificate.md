---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275864"
---
# <span data-ttu-id="aedc2-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="aedc2-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="aedc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aedc2-102">SYNOPSIS</span></span>
<span data-ttu-id="aedc2-103">Küme güvenliği için kullanılan küme sertifikasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="aedc2-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="aedc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aedc2-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aedc2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aedc2-105">DESCRIPTION</span></span>
<span data-ttu-id="aedc2-106">Kümede zaten kullanımda olan başka bir geçerli sertifika olduğu sürece, kümeden küme sertifikasını kaldırmak için **Remove-AzServiceFabricClusterCertificate** kullanın.</span><span class="sxs-lookup"><span data-stu-id="aedc2-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="aedc2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aedc2-107">EXAMPLES</span></span>

### <span data-ttu-id="aedc2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aedc2-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="aedc2-109">Bu komut, küme güvenliği için parmak izi 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A kullanılmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aedc2-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="aedc2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aedc2-110">PARAMETERS</span></span>

### <span data-ttu-id="aedc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aedc2-111">-DefaultProfile</span></span>
<span data-ttu-id="aedc2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aedc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aedc2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="aedc2-113">-Name</span></span>
<span data-ttu-id="aedc2-114">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="aedc2-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aedc2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aedc2-115">-ResourceGroupName</span></span>
<span data-ttu-id="aedc2-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aedc2-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aedc2-117">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="aedc2-117">-Thumbprint</span></span>
<span data-ttu-id="aedc2-118">Kaldırılacak küme parmak izini belirtin.</span><span class="sxs-lookup"><span data-stu-id="aedc2-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aedc2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="aedc2-119">-Confirm</span></span>
<span data-ttu-id="aedc2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aedc2-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aedc2-121">-WhatIf</span></span>
<span data-ttu-id="aedc2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aedc2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aedc2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aedc2-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aedc2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aedc2-124">CommonParameters</span></span>
<span data-ttu-id="aedc2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aedc2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aedc2-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aedc2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aedc2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aedc2-127">INPUTS</span></span>

### <span data-ttu-id="aedc2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aedc2-128">System.String</span></span>

## <span data-ttu-id="aedc2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aedc2-129">OUTPUTS</span></span>

### <span data-ttu-id="aedc2-130">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="aedc2-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="aedc2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aedc2-131">NOTES</span></span>

## <span data-ttu-id="aedc2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aedc2-132">RELATED LINKS</span></span>
