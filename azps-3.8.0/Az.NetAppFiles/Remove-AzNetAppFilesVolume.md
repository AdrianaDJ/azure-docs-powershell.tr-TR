---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: cbbf68dfa3d71da40e22dc608c4933b65f953c7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937246"
---
# <span data-ttu-id="5f99a-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5f99a-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="5f99a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f99a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f99a-103">Bir Azure NetApp dosyası (ANF) birimi siler.</span><span class="sxs-lookup"><span data-stu-id="5f99a-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="5f99a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f99a-104">SYNTAX</span></span>

### <span data-ttu-id="5f99a-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f99a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f99a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f99a-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f99a-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5f99a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f99a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f99a-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f99a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f99a-109">DESCRIPTION</span></span>
<span data-ttu-id="5f99a-110">**Remove-AzNetAppFilesVolume** cmdlet 'i ANF sesini siler.</span><span class="sxs-lookup"><span data-stu-id="5f99a-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="5f99a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f99a-111">EXAMPLES</span></span>

### <span data-ttu-id="5f99a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5f99a-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="5f99a-113">Bu komut, ANF birimini "MyAnfVolume" siler.</span><span class="sxs-lookup"><span data-stu-id="5f99a-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="5f99a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f99a-114">PARAMETERS</span></span>

### <span data-ttu-id="5f99a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5f99a-115">-AccountName</span></span>
<span data-ttu-id="5f99a-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="5f99a-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="5f99a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f99a-117">-DefaultProfile</span></span>
<span data-ttu-id="5f99a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f99a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f99a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f99a-119">-InputObject</span></span>
<span data-ttu-id="5f99a-120">Kaldırılacak birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="5f99a-120">The volume object to remove</span></span>

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

### <span data-ttu-id="5f99a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f99a-121">-Name</span></span>
<span data-ttu-id="5f99a-122">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="5f99a-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="5f99a-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5f99a-123">-PassThru</span></span>
<span data-ttu-id="5f99a-124">Belirtilen birimin başarıyla kaldırılıp kaldırılmadığını döndürme</span><span class="sxs-lookup"><span data-stu-id="5f99a-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="5f99a-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5f99a-125">-PoolName</span></span>
<span data-ttu-id="5f99a-126">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="5f99a-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="5f99a-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="5f99a-127">-PoolObject</span></span>
<span data-ttu-id="5f99a-128">Kaldırılacak birimi içeren havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="5f99a-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="5f99a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f99a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5f99a-130">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="5f99a-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="5f99a-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5f99a-131">-ResourceId</span></span>
<span data-ttu-id="5f99a-132">ANF biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5f99a-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="5f99a-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f99a-133">-Confirm</span></span>
<span data-ttu-id="5f99a-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f99a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f99a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f99a-135">-WhatIf</span></span>
<span data-ttu-id="5f99a-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f99a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f99a-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f99a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f99a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f99a-138">CommonParameters</span></span>
<span data-ttu-id="5f99a-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f99a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5f99a-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f99a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f99a-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f99a-141">INPUTS</span></span>

### <span data-ttu-id="5f99a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5f99a-142">System.String</span></span>

### <span data-ttu-id="5f99a-143">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5f99a-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="5f99a-144">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5f99a-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5f99a-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f99a-145">OUTPUTS</span></span>

### <span data-ttu-id="5f99a-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f99a-146">System.Boolean</span></span>

## <span data-ttu-id="5f99a-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f99a-147">NOTES</span></span>

## <span data-ttu-id="5f99a-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f99a-148">RELATED LINKS</span></span>
