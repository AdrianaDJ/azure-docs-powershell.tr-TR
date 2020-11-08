---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273954"
---
# <span data-ttu-id="02ba0-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="02ba0-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="02ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="02ba0-103">Parmak izi veya ortak ada göre remvoe istemci sertifikası.</span><span class="sxs-lookup"><span data-stu-id="02ba0-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="02ba0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02ba0-104">SYNTAX</span></span>

### <span data-ttu-id="02ba0-105">ClientCertByTpByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02ba0-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ba0-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="02ba0-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02ba0-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="02ba0-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02ba0-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="02ba0-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ba0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="02ba0-109">DESCRIPTION</span></span>
<span data-ttu-id="02ba0-110">Parmak izi veya ortak ada göre remvoe istemci sertifikası.</span><span class="sxs-lookup"><span data-stu-id="02ba0-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="02ba0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02ba0-111">EXAMPLES</span></span>

### <span data-ttu-id="02ba0-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02ba0-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="02ba0-113">İstemci sertifikasını ortak ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="02ba0-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="02ba0-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="02ba0-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="02ba0-115">Parmak izli istemci sertifikasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="02ba0-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="02ba0-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="02ba0-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="02ba0-117">Parmak iziyle istemci sertifikasını parmak izli kaldırma.</span><span class="sxs-lookup"><span data-stu-id="02ba0-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="02ba0-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02ba0-118">PARAMETERS</span></span>

### <span data-ttu-id="02ba0-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="02ba0-119">-AsJob</span></span>
<span data-ttu-id="02ba0-120">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="02ba0-120">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ba0-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="02ba0-121">-CommonName</span></span>
<span data-ttu-id="02ba0-122">İstemci sertifikası ortak adı.</span><span class="sxs-lookup"><span data-stu-id="02ba0-122">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ba0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ba0-123">-DefaultProfile</span></span>
<span data-ttu-id="02ba0-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02ba0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ba0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02ba0-125">-InputObject</span></span>
<span data-ttu-id="02ba0-126">Yönetilen küme kaynağı</span><span class="sxs-lookup"><span data-stu-id="02ba0-126">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02ba0-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="02ba0-127">-Name</span></span>
<span data-ttu-id="02ba0-128">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="02ba0-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ba0-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="02ba0-129">-PassThru</span></span>
<span data-ttu-id="02ba0-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="02ba0-130">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ba0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ba0-131">-ResourceGroupName</span></span>
<span data-ttu-id="02ba0-132">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="02ba0-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ba0-133">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="02ba0-133">-Thumbprint</span></span>
<span data-ttu-id="02ba0-134">İstemci sertifikası parmak izi.</span><span class="sxs-lookup"><span data-stu-id="02ba0-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ba0-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="02ba0-135">-Confirm</span></span>
<span data-ttu-id="02ba0-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02ba0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ba0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ba0-137">-WhatIf</span></span>
<span data-ttu-id="02ba0-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02ba0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ba0-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02ba0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ba0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ba0-140">CommonParameters</span></span>
<span data-ttu-id="02ba0-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02ba0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ba0-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02ba0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ba0-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02ba0-143">INPUTS</span></span>

### <span data-ttu-id="02ba0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="02ba0-144">System.String</span></span>

## <span data-ttu-id="02ba0-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02ba0-145">OUTPUTS</span></span>

### <span data-ttu-id="02ba0-146">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="02ba0-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="02ba0-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02ba0-147">NOTES</span></span>

## <span data-ttu-id="02ba0-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02ba0-148">RELATED LINKS</span></span>
