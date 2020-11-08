---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278386"
---
# <span data-ttu-id="26a2f-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="26a2f-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="26a2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="26a2f-103">Bir Azure NetApp dosyası (ANF) birimi siler.</span><span class="sxs-lookup"><span data-stu-id="26a2f-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="26a2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26a2f-104">SYNTAX</span></span>

### <span data-ttu-id="26a2f-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26a2f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a2f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26a2f-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a2f-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="26a2f-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a2f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26a2f-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26a2f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="26a2f-109">DESCRIPTION</span></span>
<span data-ttu-id="26a2f-110">**Remove-AzNetAppFilesVolume** cmdlet 'i ANF sesini siler.</span><span class="sxs-lookup"><span data-stu-id="26a2f-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="26a2f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26a2f-111">EXAMPLES</span></span>

### <span data-ttu-id="26a2f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26a2f-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="26a2f-113">Bu komut, ANF birimini "MyAnfVolume" siler.</span><span class="sxs-lookup"><span data-stu-id="26a2f-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="26a2f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26a2f-114">PARAMETERS</span></span>

### <span data-ttu-id="26a2f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26a2f-115">-AccountName</span></span>
<span data-ttu-id="26a2f-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="26a2f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="26a2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a2f-117">-DefaultProfile</span></span>
<span data-ttu-id="26a2f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26a2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26a2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26a2f-119">-InputObject</span></span>
<span data-ttu-id="26a2f-120">Kaldırılacak birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="26a2f-120">The volume object to remove</span></span>

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

### <span data-ttu-id="26a2f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="26a2f-121">-Name</span></span>
<span data-ttu-id="26a2f-122">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="26a2f-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="26a2f-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="26a2f-123">-PassThru</span></span>
<span data-ttu-id="26a2f-124">Belirtilen birimin başarıyla kaldırılıp kaldırılmadığını döndürme</span><span class="sxs-lookup"><span data-stu-id="26a2f-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="26a2f-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="26a2f-125">-PoolName</span></span>
<span data-ttu-id="26a2f-126">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="26a2f-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="26a2f-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="26a2f-127">-PoolObject</span></span>
<span data-ttu-id="26a2f-128">Kaldırılacak birimi içeren havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="26a2f-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="26a2f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26a2f-129">-ResourceGroupName</span></span>
<span data-ttu-id="26a2f-130">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="26a2f-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="26a2f-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="26a2f-131">-ResourceId</span></span>
<span data-ttu-id="26a2f-132">ANF biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="26a2f-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="26a2f-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="26a2f-133">-Confirm</span></span>
<span data-ttu-id="26a2f-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26a2f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26a2f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26a2f-135">-WhatIf</span></span>
<span data-ttu-id="26a2f-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26a2f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26a2f-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26a2f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26a2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a2f-138">CommonParameters</span></span>
<span data-ttu-id="26a2f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26a2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a2f-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="26a2f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a2f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26a2f-141">INPUTS</span></span>

### <span data-ttu-id="26a2f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="26a2f-142">System.String</span></span>

### <span data-ttu-id="26a2f-143">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="26a2f-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="26a2f-144">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="26a2f-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="26a2f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26a2f-145">OUTPUTS</span></span>

### <span data-ttu-id="26a2f-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26a2f-146">System.Boolean</span></span>

## <span data-ttu-id="26a2f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26a2f-147">NOTES</span></span>

## <span data-ttu-id="26a2f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26a2f-148">RELATED LINKS</span></span>
