---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f6b21f3496f8ac05147db24de1df2ee03693fb7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760762"
---
# <span data-ttu-id="75e8b-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="75e8b-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="75e8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="75e8b-103">Bir Azure NetApp dosyası (ANF) birimi siler.</span><span class="sxs-lookup"><span data-stu-id="75e8b-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="75e8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75e8b-104">SYNTAX</span></span>

### <span data-ttu-id="75e8b-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75e8b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e8b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75e8b-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e8b-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="75e8b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75e8b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75e8b-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75e8b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="75e8b-109">DESCRIPTION</span></span>
<span data-ttu-id="75e8b-110">**Remove-AzNetAppFilesVolume** cmdlet 'i ANF sesini siler.</span><span class="sxs-lookup"><span data-stu-id="75e8b-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="75e8b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75e8b-111">EXAMPLES</span></span>

### <span data-ttu-id="75e8b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="75e8b-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="75e8b-113">Bu komut, ANF birimini "MyAnfVolume" siler.</span><span class="sxs-lookup"><span data-stu-id="75e8b-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="75e8b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75e8b-114">PARAMETERS</span></span>

### <span data-ttu-id="75e8b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75e8b-115">-AccountName</span></span>
<span data-ttu-id="75e8b-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="75e8b-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="75e8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e8b-117">-DefaultProfile</span></span>
<span data-ttu-id="75e8b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75e8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e8b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75e8b-119">-InputObject</span></span>
<span data-ttu-id="75e8b-120">Kaldırılacak birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="75e8b-120">The volume object to remove</span></span>

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

### <span data-ttu-id="75e8b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="75e8b-121">-Name</span></span>
<span data-ttu-id="75e8b-122">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="75e8b-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="75e8b-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="75e8b-123">-PassThru</span></span>
<span data-ttu-id="75e8b-124">Belirtilen birimin başarıyla kaldırılıp kaldırılmadığını döndürme</span><span class="sxs-lookup"><span data-stu-id="75e8b-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="75e8b-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="75e8b-125">-PoolName</span></span>
<span data-ttu-id="75e8b-126">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="75e8b-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="75e8b-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="75e8b-127">-PoolObject</span></span>
<span data-ttu-id="75e8b-128">Kaldırılacak birimi içeren havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="75e8b-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="75e8b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e8b-129">-ResourceGroupName</span></span>
<span data-ttu-id="75e8b-130">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="75e8b-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="75e8b-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="75e8b-131">-ResourceId</span></span>
<span data-ttu-id="75e8b-132">ANF biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="75e8b-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="75e8b-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="75e8b-133">-Confirm</span></span>
<span data-ttu-id="75e8b-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75e8b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75e8b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75e8b-135">-WhatIf</span></span>
<span data-ttu-id="75e8b-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75e8b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75e8b-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75e8b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75e8b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e8b-138">CommonParameters</span></span>
<span data-ttu-id="75e8b-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75e8b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="75e8b-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e8b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e8b-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75e8b-141">INPUTS</span></span>

### <span data-ttu-id="75e8b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="75e8b-142">System.String</span></span>

### <span data-ttu-id="75e8b-143">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="75e8b-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="75e8b-144">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="75e8b-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="75e8b-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75e8b-145">OUTPUTS</span></span>

### <span data-ttu-id="75e8b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75e8b-146">System.Boolean</span></span>

## <span data-ttu-id="75e8b-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75e8b-147">NOTES</span></span>

## <span data-ttu-id="75e8b-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75e8b-148">RELATED LINKS</span></span>
