---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760764"
---
# <span data-ttu-id="6a90b-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6a90b-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="6a90b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a90b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a90b-103">Azure NetApp dosyalarını (ANF) siler.</span><span class="sxs-lookup"><span data-stu-id="6a90b-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="6a90b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a90b-104">SYNTAX</span></span>

### <span data-ttu-id="6a90b-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a90b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a90b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a90b-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a90b-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6a90b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a90b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a90b-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a90b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a90b-109">DESCRIPTION</span></span>
<span data-ttu-id="6a90b-110">**Remove-AzNetAppFilesPool** cmdlet 'i ANF havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="6a90b-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="6a90b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a90b-111">EXAMPLES</span></span>

### <span data-ttu-id="6a90b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a90b-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="6a90b-113">Bu komut, "MyAnfPool" ANF havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="6a90b-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="6a90b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a90b-114">PARAMETERS</span></span>

### <span data-ttu-id="6a90b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6a90b-115">-AccountName</span></span>
<span data-ttu-id="6a90b-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="6a90b-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="6a90b-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6a90b-117">-AccountObject</span></span>
<span data-ttu-id="6a90b-118">Kaldırılacak havuzu içeren hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="6a90b-118">The account object containing the pool to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a90b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a90b-119">-DefaultProfile</span></span>
<span data-ttu-id="6a90b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a90b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a90b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a90b-121">-InputObject</span></span>
<span data-ttu-id="6a90b-122">Kaldırılacak havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="6a90b-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a90b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a90b-123">-Name</span></span>
<span data-ttu-id="6a90b-124">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="6a90b-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a90b-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6a90b-125">-PassThru</span></span>
<span data-ttu-id="6a90b-126">Belirtilen havuzun başarıyla kaldırıldığını geri döndürme</span><span class="sxs-lookup"><span data-stu-id="6a90b-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="6a90b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a90b-127">-ResourceGroupName</span></span>
<span data-ttu-id="6a90b-128">ANF havuzunun kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="6a90b-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="6a90b-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6a90b-129">-ResourceId</span></span>
<span data-ttu-id="6a90b-130">ANF havuzunun kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6a90b-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="6a90b-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a90b-131">-Confirm</span></span>
<span data-ttu-id="6a90b-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a90b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a90b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a90b-133">-WhatIf</span></span>
<span data-ttu-id="6a90b-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a90b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a90b-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a90b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a90b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a90b-136">CommonParameters</span></span>
<span data-ttu-id="6a90b-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a90b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6a90b-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a90b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a90b-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a90b-139">INPUTS</span></span>

### <span data-ttu-id="6a90b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6a90b-140">System.String</span></span>

### <span data-ttu-id="6a90b-141">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6a90b-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="6a90b-142">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6a90b-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6a90b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a90b-143">OUTPUTS</span></span>

### <span data-ttu-id="6a90b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a90b-144">System.Boolean</span></span>

## <span data-ttu-id="6a90b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a90b-145">NOTES</span></span>

## <span data-ttu-id="6a90b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a90b-146">RELATED LINKS</span></span>
