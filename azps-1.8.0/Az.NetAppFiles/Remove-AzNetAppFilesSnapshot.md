---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 16eb962245502338c7b12f6e5abf20a9bc04b83f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760765"
---
# <span data-ttu-id="5ed48-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="5ed48-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="5ed48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ed48-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed48-103">Azure NetApp dosyaları (ANF) anlık görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="5ed48-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="5ed48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ed48-104">SYNTAX</span></span>

### <span data-ttu-id="5ed48-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ed48-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed48-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5ed48-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed48-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ed48-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed48-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ed48-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ed48-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ed48-109">DESCRIPTION</span></span>
<span data-ttu-id="5ed48-110">**Remove-AzNetAppFilesSnapshot** cmdlet 'i ANF anlık görüntüsünü siler.</span><span class="sxs-lookup"><span data-stu-id="5ed48-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="5ed48-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ed48-111">EXAMPLES</span></span>

### <span data-ttu-id="5ed48-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ed48-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="5ed48-113">Bu komut, ANF anlık görüntüsünü "MyAnfSnapshot" siler.</span><span class="sxs-lookup"><span data-stu-id="5ed48-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="5ed48-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ed48-114">PARAMETERS</span></span>

### <span data-ttu-id="5ed48-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5ed48-115">-AccountName</span></span>
<span data-ttu-id="5ed48-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="5ed48-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="5ed48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed48-117">-DefaultProfile</span></span>
<span data-ttu-id="5ed48-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ed48-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ed48-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ed48-119">-InputObject</span></span>
<span data-ttu-id="5ed48-120">Kaldırılacak anlık görüntü nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ed48-120">The snapshot object to remove</span></span>

```yaml
Type: PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed48-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ed48-121">-Name</span></span>
<span data-ttu-id="5ed48-122">ANF anlık görüntüsünün adı</span><span class="sxs-lookup"><span data-stu-id="5ed48-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed48-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5ed48-123">-PassThru</span></span>
<span data-ttu-id="5ed48-124">Belirtilen birimin başarıyla kaldırılıp kaldırılmadığını döndürme</span><span class="sxs-lookup"><span data-stu-id="5ed48-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed48-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5ed48-125">-PoolName</span></span>
<span data-ttu-id="5ed48-126">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="5ed48-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="5ed48-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed48-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ed48-128">ANF anlık görüntüsünün kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="5ed48-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="5ed48-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5ed48-129">-ResourceId</span></span>
<span data-ttu-id="5ed48-130">ANF anlık görüntüsünün kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5ed48-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="5ed48-131">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="5ed48-131">-VolumeName</span></span>
<span data-ttu-id="5ed48-132">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="5ed48-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="5ed48-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="5ed48-133">-VolumeObject</span></span>
<span data-ttu-id="5ed48-134">Kaldırılacak anlık görüntüyü içeren birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ed48-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed48-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ed48-135">-Confirm</span></span>
<span data-ttu-id="5ed48-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ed48-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ed48-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ed48-137">-WhatIf</span></span>
<span data-ttu-id="5ed48-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ed48-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ed48-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ed48-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ed48-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed48-140">CommonParameters</span></span>
<span data-ttu-id="5ed48-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ed48-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5ed48-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed48-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed48-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ed48-143">INPUTS</span></span>

### <span data-ttu-id="5ed48-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5ed48-144">System.String</span></span>

### <span data-ttu-id="5ed48-145">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5ed48-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="5ed48-146">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="5ed48-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="5ed48-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ed48-147">OUTPUTS</span></span>

### <span data-ttu-id="5ed48-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ed48-148">System.Boolean</span></span>

## <span data-ttu-id="5ed48-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ed48-149">NOTES</span></span>

## <span data-ttu-id="5ed48-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ed48-150">RELATED LINKS</span></span>
