---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319557"
---
# <span data-ttu-id="b276a-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b276a-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="b276a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b276a-102">SYNOPSIS</span></span>
<span data-ttu-id="b276a-103">Belirtilen HDInsight kümesinin disk şifreleme anahtarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b276a-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="b276a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b276a-104">SYNTAX</span></span>

### <span data-ttu-id="b276a-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b276a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b276a-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b276a-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b276a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b276a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b276a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b276a-108">DESCRIPTION</span></span>
<span data-ttu-id="b276a-109">Belirtilen HDInsight kümesinin disk şifreleme anahtarını döndürün.</span><span class="sxs-lookup"><span data-stu-id="b276a-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="b276a-110">Bu işlem için, kümenin hem geçerli anahtara hem de hedeflenen yeni anahtara erişimi olmalıdır, aksi takdirde anahtar Döndür işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="b276a-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="b276a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b276a-111">EXAMPLES</span></span>

### <span data-ttu-id="b276a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b276a-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="b276a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b276a-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="b276a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b276a-114">PARAMETERS</span></span>

### <span data-ttu-id="b276a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b276a-115">-DefaultProfile</span></span>
<span data-ttu-id="b276a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b276a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b276a-117">-Encryptionanahtaradı</span><span class="sxs-lookup"><span data-stu-id="b276a-117">-EncryptionKeyName</span></span>
<span data-ttu-id="b276a-118">Şifreleme anahtarı adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b276a-118">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="b276a-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="b276a-120">Şifreleme anahtarı sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b276a-120">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-121">-Şifrelemem</span><span class="sxs-lookup"><span data-stu-id="b276a-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="b276a-122">Şifreleme Kasası URI 'sini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b276a-122">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b276a-123">-InputObject</span></span>
<span data-ttu-id="b276a-124">Giriş nesnesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b276a-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b276a-125">-Name</span></span>
<span data-ttu-id="b276a-126">Kümenin adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b276a-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b276a-127">-ResourceGroupName</span></span>
<span data-ttu-id="b276a-128">Kaynak grubunun adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b276a-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b276a-129">-ResourceId</span></span>
<span data-ttu-id="b276a-130">Kaynak kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b276a-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b276a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="b276a-131">-Confirm</span></span>
<span data-ttu-id="b276a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b276a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b276a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b276a-133">-WhatIf</span></span>
<span data-ttu-id="b276a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b276a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b276a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b276a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b276a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b276a-136">CommonParameters</span></span>
<span data-ttu-id="b276a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b276a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b276a-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b276a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b276a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b276a-139">INPUTS</span></span>

### <span data-ttu-id="b276a-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b276a-140">None</span></span>

## <span data-ttu-id="b276a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b276a-141">OUTPUTS</span></span>

### <span data-ttu-id="b276a-142">Microsoft. Azure. Management. HDInsight. modeller. Cluster</span><span class="sxs-lookup"><span data-stu-id="b276a-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="b276a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b276a-143">NOTES</span></span>

## <span data-ttu-id="b276a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b276a-144">RELATED LINKS</span></span>

[<span data-ttu-id="b276a-145">Müşteri tarafından yönetilen anahtar disk şifrelemesi</span><span class="sxs-lookup"><span data-stu-id="b276a-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
