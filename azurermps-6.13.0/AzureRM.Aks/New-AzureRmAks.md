---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: f91b4f2afdb1c6aaf7cbac16f952a333d3d362b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763518"
---
# <span data-ttu-id="ac9ff-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="ac9ff-101">New-AzureRmAks</span></span>

## <span data-ttu-id="ac9ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9ff-103">Yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac9ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac9ff-104">SYNTAX</span></span>

```
New-AzureRmAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac9ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac9ff-105">DESCRIPTION</span></span>

<span data-ttu-id="ac9ff-106">Yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ac9ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac9ff-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9ff-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ac9ff-108">Example 1</span></span>

<span data-ttu-id="ac9ff-109">Varsayılan params ile yeni bir yönetilen Kubernetes kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="ac9ff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac9ff-110">PARAMETERS</span></span>

### <span data-ttu-id="ac9ff-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="ac9ff-111">-AdminUserName</span></span>
<span data-ttu-id="ac9ff-112">Linux sanal makinelerinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ac9ff-113">-AsJob</span></span>
<span data-ttu-id="ac9ff-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ac9ff-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac9ff-115">-Clientidanvseçsecret</span><span class="sxs-lookup"><span data-stu-id="ac9ff-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="ac9ff-116">AAD uygulaması/hizmet sorumlusu ile ilişkilendirilmiş istemci kimliği ve istemci parolası.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9ff-117">-DefaultProfile</span></span>
<span data-ttu-id="ac9ff-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9ff-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="ac9ff-119">-DnsNamePrefix</span></span>
<span data-ttu-id="ac9ff-120">Kümenin DNS adı öneki.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ac9ff-121">-Force</span></span>
<span data-ttu-id="ac9ff-122">Zaten var olsa bile küme oluştur</span><span class="sxs-lookup"><span data-stu-id="ac9ff-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="ac9ff-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="ac9ff-123">-KubernetesVersion</span></span>
<span data-ttu-id="ac9ff-124">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="ac9ff-125">-Location</span></span>
<span data-ttu-id="ac9ff-126">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-126">Azure location for the cluster.</span></span>
<span data-ttu-id="ac9ff-127">Kaynak grubunun konumunu varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="ac9ff-128">-Name</span></span>
<span data-ttu-id="ac9ff-129">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="ac9ff-130">-NodeCount</span></span>
<span data-ttu-id="ac9ff-131">Düğüm havuzları için varsayılan düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="ac9ff-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="ac9ff-133">Düğüm havuzundaki her düğümün işletim sistemi diskinin boyutu.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="ac9ff-134">En az 30 GB.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-134">Minimum 30 GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-135">-Edevmboyut</span><span class="sxs-lookup"><span data-stu-id="ac9ff-135">-NodeVmSize</span></span>
<span data-ttu-id="ac9ff-136">Sanal makinenin boyutu.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-136">The size of the Virtual Machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac9ff-137">-ResourceGroupName</span></span>
<span data-ttu-id="ac9ff-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-138">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="ac9ff-139">-SshKeyValue</span></span>
<span data-ttu-id="ac9ff-140">SSH anahtar dosyası veya anahtar dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="ac9ff-141">{HOME}/.ssh/id_rsa. pub varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ac9ff-142">-Tag</span></span>
<span data-ttu-id="ac9ff-143">Kaynağa uygulanacak Etiketler</span><span class="sxs-lookup"><span data-stu-id="ac9ff-143">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9ff-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="ac9ff-144">-Confirm</span></span>
<span data-ttu-id="ac9ff-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac9ff-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac9ff-146">-WhatIf</span></span>
<span data-ttu-id="ac9ff-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac9ff-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac9ff-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9ff-149">CommonParameters</span></span>
<span data-ttu-id="ac9ff-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac9ff-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9ff-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9ff-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9ff-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac9ff-152">INPUTS</span></span>

### <span data-ttu-id="ac9ff-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ac9ff-153">None</span></span>

## <span data-ttu-id="ac9ff-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac9ff-154">OUTPUTS</span></span>

### <span data-ttu-id="ac9ff-155">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ac9ff-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ac9ff-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac9ff-156">NOTES</span></span>

## <span data-ttu-id="ac9ff-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac9ff-157">RELATED LINKS</span></span>
