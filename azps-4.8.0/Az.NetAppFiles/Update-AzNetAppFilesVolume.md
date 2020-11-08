---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: c28b53fcd9b65198554f34cacd6f628d977e703a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107727"
---
# <span data-ttu-id="b6004-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b6004-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="b6004-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6004-102">SYNOPSIS</span></span>
<span data-ttu-id="b6004-103">Azure NetApp dosyaları (ANF) birimini sağlanan isteğe bağlı değiştiricilere göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b6004-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="b6004-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6004-104">SYNTAX</span></span>

### <span data-ttu-id="b6004-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6004-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6004-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6004-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6004-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b6004-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6004-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6004-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6004-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6004-109">DESCRIPTION</span></span>
<span data-ttu-id="b6004-110">**Update-AzNetAppFilesVolume** cmdlet 'i ANF sesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b6004-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="b6004-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6004-111">EXAMPLES</span></span>

### <span data-ttu-id="b6004-112">Örnek 1: ANF sesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b6004-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="b6004-113">Bu komut, ANF birimini "MyAnfVolume" yeni UsageThreshold boyutuyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b6004-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="b6004-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6004-114">PARAMETERS</span></span>

### <span data-ttu-id="b6004-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6004-115">-AccountName</span></span>
<span data-ttu-id="b6004-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="b6004-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6004-117">-DefaultProfile</span></span>
<span data-ttu-id="b6004-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6004-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6004-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="b6004-119">-ExportPolicy</span></span>
<span data-ttu-id="b6004-120">Dışarı aktarma ilkesini temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="b6004-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6004-121">-InputObject</span></span>
<span data-ttu-id="b6004-122">Güncelleştirilecek birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="b6004-122">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="b6004-123">-Location</span></span>
<span data-ttu-id="b6004-124">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="b6004-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6004-125">-Name</span></span>
<span data-ttu-id="b6004-126">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="b6004-126">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b6004-127">-PoolName</span></span>
<span data-ttu-id="b6004-128">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="b6004-128">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-129">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="b6004-129">-PoolObject</span></span>
<span data-ttu-id="b6004-130">Güncelleştirilecek birimi içeren havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="b6004-130">The pool object containing the volume to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6004-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6004-132">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="b6004-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b6004-133">-ResourceId</span></span>
<span data-ttu-id="b6004-134">ANF biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b6004-134">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="b6004-135">-ServiceLevel</span></span>
<span data-ttu-id="b6004-136">ANF biriminin hizmet düzeyi</span><span class="sxs-lookup"><span data-stu-id="b6004-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="b6004-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b6004-137">-Tag</span></span>
<span data-ttu-id="b6004-138">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6004-138">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="b6004-139">-UsageThreshold</span></span>
<span data-ttu-id="b6004-140">Bayt cinsinden bir dosya sistemi için izin verilen maksimum depolama kotası</span><span class="sxs-lookup"><span data-stu-id="b6004-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6004-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6004-141">-Confirm</span></span>
<span data-ttu-id="b6004-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6004-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6004-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6004-143">-WhatIf</span></span>
<span data-ttu-id="b6004-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6004-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6004-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6004-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6004-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6004-146">CommonParameters</span></span>
<span data-ttu-id="b6004-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6004-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6004-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6004-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6004-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6004-149">INPUTS</span></span>

### <span data-ttu-id="b6004-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b6004-150">System.String</span></span>

### <span data-ttu-id="b6004-151">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6004-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="b6004-152">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b6004-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b6004-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6004-153">OUTPUTS</span></span>

### <span data-ttu-id="b6004-154">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b6004-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b6004-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6004-155">NOTES</span></span>

## <span data-ttu-id="b6004-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6004-156">RELATED LINKS</span></span>
