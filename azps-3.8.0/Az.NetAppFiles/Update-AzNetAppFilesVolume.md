---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: d59bd7bea42e442aace3817f985098c4b2344ce4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937238"
---
# <span data-ttu-id="d7ec6-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d7ec6-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d7ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ec6-103">Azure NetApp dosyaları (ANF) birimini sağlanan isteğe bağlı değiştiricilere göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="d7ec6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7ec6-104">SYNTAX</span></span>

### <span data-ttu-id="d7ec6-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7ec6-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7ec6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7ec6-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7ec6-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d7ec6-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7ec6-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7ec6-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7ec6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7ec6-109">DESCRIPTION</span></span>
<span data-ttu-id="d7ec6-110">**Update-AzNetAppFilesVolume** cmdlet 'i ANF sesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="d7ec6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7ec6-111">EXAMPLES</span></span>

### <span data-ttu-id="d7ec6-112">Örnek 1: ANF sesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d7ec6-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="d7ec6-113">Bu komut, ANF birimini "MyAnfVolume" yeni UsageThreshold boyutuyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="d7ec6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7ec6-114">PARAMETERS</span></span>

### <span data-ttu-id="d7ec6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7ec6-115">-AccountName</span></span>
<span data-ttu-id="d7ec6-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="d7ec6-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ec6-117">-DefaultProfile</span></span>
<span data-ttu-id="d7ec6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="d7ec6-119">-ExportPolicy</span></span>
<span data-ttu-id="d7ec6-120">Dışarı aktarma ilkesini temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="d7ec6-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7ec6-121">-InputObject</span></span>
<span data-ttu-id="d7ec6-122">Güncelleştirilecek birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="d7ec6-122">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="d7ec6-123">-Location</span></span>
<span data-ttu-id="d7ec6-124">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="d7ec6-124">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7ec6-125">-Name</span></span>
<span data-ttu-id="d7ec6-126">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="d7ec6-126">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d7ec6-127">-PoolName</span></span>
<span data-ttu-id="d7ec6-128">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="d7ec6-128">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-129">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="d7ec6-129">-PoolObject</span></span>
<span data-ttu-id="d7ec6-130">Güncelleştirilecek birimi içeren havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="d7ec6-130">The pool object containing the volume to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ec6-131">-ResourceGroupName</span></span>
<span data-ttu-id="d7ec6-132">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="d7ec6-132">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d7ec6-133">-ResourceId</span></span>
<span data-ttu-id="d7ec6-134">ANF biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d7ec6-134">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="d7ec6-135">-ServiceLevel</span></span>
<span data-ttu-id="d7ec6-136">ANF biriminin hizmet düzeyi</span><span class="sxs-lookup"><span data-stu-id="d7ec6-136">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d7ec6-137">-Tag</span></span>
<span data-ttu-id="d7ec6-138">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="d7ec6-138">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="d7ec6-139">-UsageThreshold</span></span>
<span data-ttu-id="d7ec6-140">Bayt cinsinden bir dosya sistemi için izin verilen maksimum depolama kotası</span><span class="sxs-lookup"><span data-stu-id="d7ec6-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ec6-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7ec6-141">-Confirm</span></span>
<span data-ttu-id="d7ec6-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ec6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ec6-143">-WhatIf</span></span>
<span data-ttu-id="d7ec6-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7ec6-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ec6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ec6-146">CommonParameters</span></span>
<span data-ttu-id="d7ec6-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d7ec6-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ec6-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ec6-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7ec6-149">INPUTS</span></span>

### <span data-ttu-id="d7ec6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d7ec6-150">System.String</span></span>

### <span data-ttu-id="d7ec6-151">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d7ec6-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="d7ec6-152">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d7ec6-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d7ec6-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7ec6-153">OUTPUTS</span></span>

### <span data-ttu-id="d7ec6-154">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d7ec6-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d7ec6-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7ec6-155">NOTES</span></span>

## <span data-ttu-id="d7ec6-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7ec6-156">RELATED LINKS</span></span>