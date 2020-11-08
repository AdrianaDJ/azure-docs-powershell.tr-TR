---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274185"
---
# <span data-ttu-id="e183b-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e183b-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="e183b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e183b-102">SYNOPSIS</span></span>
<span data-ttu-id="e183b-103">Bir cihazın kenar depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e183b-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="e183b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e183b-104">SYNTAX</span></span>

### <span data-ttu-id="e183b-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e183b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e183b-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e183b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e183b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e183b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e183b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e183b-108">DESCRIPTION</span></span>
<span data-ttu-id="e183b-109">**Remove-AzDataBoxEdgeStorageAccount** cmdlet 'i, bir veri kutusu uç aygıtının Ilişkili kenar depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e183b-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="e183b-110">Cmdlet 'teki bir parametre olarak kaldırılacak Edge depolama hesabının adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e183b-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="e183b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e183b-111">EXAMPLES</span></span>

### <span data-ttu-id="e183b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e183b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="e183b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e183b-113">PARAMETERS</span></span>

### <span data-ttu-id="e183b-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="e183b-114">-AsJob</span></span>
<span data-ttu-id="e183b-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e183b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e183b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e183b-116">-DefaultProfile</span></span>
<span data-ttu-id="e183b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e183b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e183b-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="e183b-118">-DeviceName</span></span>
<span data-ttu-id="e183b-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="e183b-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e183b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e183b-120">-InputObject</span></span>
<span data-ttu-id="e183b-121">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="e183b-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e183b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e183b-122">-Name</span></span>
<span data-ttu-id="e183b-123">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="e183b-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e183b-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e183b-124">-PassThru</span></span>
<span data-ttu-id="e183b-125">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="e183b-125">returns true if successful</span></span>

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

### <span data-ttu-id="e183b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e183b-126">-ResourceGroupName</span></span>
<span data-ttu-id="e183b-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e183b-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e183b-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e183b-128">-ResourceId</span></span>
<span data-ttu-id="e183b-129">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e183b-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e183b-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="e183b-130">-Confirm</span></span>
<span data-ttu-id="e183b-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e183b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e183b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e183b-132">-WhatIf</span></span>
<span data-ttu-id="e183b-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e183b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e183b-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e183b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e183b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e183b-135">CommonParameters</span></span>
<span data-ttu-id="e183b-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e183b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e183b-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e183b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e183b-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e183b-138">INPUTS</span></span>

### <span data-ttu-id="e183b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e183b-139">System.String</span></span>

### <span data-ttu-id="e183b-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e183b-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="e183b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e183b-141">OUTPUTS</span></span>

### <span data-ttu-id="e183b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e183b-142">System.Boolean</span></span>

## <span data-ttu-id="e183b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e183b-143">NOTES</span></span>

## <span data-ttu-id="e183b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e183b-144">RELATED LINKS</span></span>
