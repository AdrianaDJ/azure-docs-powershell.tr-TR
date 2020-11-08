---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107588"
---
# <span data-ttu-id="08e01-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="08e01-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="08e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08e01-102">SYNOPSIS</span></span>
<span data-ttu-id="08e01-103">Kümeye sertifika ortak adı veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="08e01-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="08e01-104">Bu işlem, sertifikayı istemci kimlik doğrulama amaçları için kümenin içine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="08e01-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="08e01-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08e01-105">SYNTAX</span></span>

### <span data-ttu-id="08e01-106">ClientCertByTpByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="08e01-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08e01-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="08e01-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08e01-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="08e01-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08e01-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="08e01-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08e01-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="08e01-110">DESCRIPTION</span></span>
<span data-ttu-id="08e01-111">Kümeye sertifika ortak adı veya parmak izi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="08e01-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="08e01-112">Bu işlem, sertifikayı istemci kimlik doğrulama amaçları için kümenin içine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="08e01-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="08e01-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08e01-113">EXAMPLES</span></span>

### <span data-ttu-id="08e01-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08e01-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="08e01-115">Bu komut, ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' parmak izine sahip sertifikayı kümeye ekler; böylece istemci kümeyle iletişim kurmak için sertifikayı yönetici olarak kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="08e01-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="08e01-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="08e01-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="08e01-117">Bu komut, ortak adı ' Contoso.com ' ve 2 veren olan bir salt okunur istemci sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="08e01-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="08e01-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="08e01-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="08e01-119">Bu komut, yöneltme ile ortak adı ' Contoso.com ' ve 2 veren olan bir salt okunur istemci sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="08e01-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="08e01-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08e01-120">PARAMETERS</span></span>

### <span data-ttu-id="08e01-121">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="08e01-121">-Admin</span></span>
<span data-ttu-id="08e01-122">İstemci sertifikasının yönetici düzeyine sahip olup olmadığını belirtmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="08e01-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="08e01-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="08e01-123">-AsJob</span></span>
<span data-ttu-id="08e01-124">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="08e01-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="08e01-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="08e01-125">-CommonName</span></span>
<span data-ttu-id="08e01-126">İstemci sertifikası ortak adı.</span><span class="sxs-lookup"><span data-stu-id="08e01-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="08e01-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e01-127">-DefaultProfile</span></span>
<span data-ttu-id="08e01-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08e01-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08e01-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08e01-129">-InputObject</span></span>
<span data-ttu-id="08e01-130">Yönetilen küme kaynağı</span><span class="sxs-lookup"><span data-stu-id="08e01-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="08e01-131">-Issuerparmak Izi</span><span class="sxs-lookup"><span data-stu-id="08e01-131">-IssuerThumbprint</span></span>
<span data-ttu-id="08e01-132">İstemci sertifikası için veren parmak izleri listesi.</span><span class="sxs-lookup"><span data-stu-id="08e01-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="08e01-133">Yalnızca CommonName ile birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="08e01-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e01-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="08e01-134">-Name</span></span>
<span data-ttu-id="08e01-135">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="08e01-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e01-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e01-136">-ResourceGroupName</span></span>
<span data-ttu-id="08e01-137">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="08e01-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e01-138">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="08e01-138">-Thumbprint</span></span>
<span data-ttu-id="08e01-139">İstemci sertifikası parmak izi.</span><span class="sxs-lookup"><span data-stu-id="08e01-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e01-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="08e01-140">-Confirm</span></span>
<span data-ttu-id="08e01-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08e01-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08e01-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08e01-142">-WhatIf</span></span>
<span data-ttu-id="08e01-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08e01-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08e01-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08e01-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08e01-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e01-145">CommonParameters</span></span>
<span data-ttu-id="08e01-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08e01-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e01-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="08e01-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e01-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08e01-148">INPUTS</span></span>

### <span data-ttu-id="08e01-149">System. String</span><span class="sxs-lookup"><span data-stu-id="08e01-149">System.String</span></span>

## <span data-ttu-id="08e01-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08e01-150">OUTPUTS</span></span>

### <span data-ttu-id="08e01-151">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="08e01-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="08e01-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08e01-152">NOTES</span></span>

## <span data-ttu-id="08e01-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08e01-153">RELATED LINKS</span></span>
