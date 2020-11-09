---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321122"
---
# <span data-ttu-id="dabe1-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dabe1-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="dabe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dabe1-102">SYNOPSIS</span></span>
<span data-ttu-id="dabe1-103">Cihazda Edge depolama hesabı için depolama kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dabe1-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="dabe1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dabe1-104">SYNTAX</span></span>

### <span data-ttu-id="dabe1-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dabe1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dabe1-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dabe1-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dabe1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dabe1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dabe1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dabe1-108">DESCRIPTION</span></span>
<span data-ttu-id="dabe1-109">**Remove-AzDataBoxEdgeStorageContainer** cmdlet 'i, bir veri kutusu Edge aygıtındaki Edge depolama hesabı için ilişkili bir depolama kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dabe1-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="dabe1-110">Parametre olarak kaldırılacak depolama kapsayıcısının adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dabe1-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="dabe1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dabe1-111">EXAMPLES</span></span>

### <span data-ttu-id="dabe1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dabe1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="dabe1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dabe1-113">PARAMETERS</span></span>

### <span data-ttu-id="dabe1-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="dabe1-114">-AsJob</span></span>
<span data-ttu-id="dabe1-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dabe1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dabe1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabe1-116">-DefaultProfile</span></span>
<span data-ttu-id="dabe1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dabe1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dabe1-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="dabe1-118">-DeviceName</span></span>
<span data-ttu-id="dabe1-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="dabe1-119">Device Name</span></span>

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

### <span data-ttu-id="dabe1-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dabe1-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="dabe1-121">Var olan EdgeStorageAccount adının adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="dabe1-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="dabe1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dabe1-122">-InputObject</span></span>
<span data-ttu-id="dabe1-123">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="dabe1-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dabe1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="dabe1-124">-Name</span></span>
<span data-ttu-id="dabe1-125">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="dabe1-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabe1-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dabe1-126">-PassThru</span></span>
<span data-ttu-id="dabe1-127">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="dabe1-127">returns true if successful</span></span>

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

### <span data-ttu-id="dabe1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabe1-128">-ResourceGroupName</span></span>
<span data-ttu-id="dabe1-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="dabe1-129">Resource Group Name</span></span>

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

### <span data-ttu-id="dabe1-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dabe1-130">-ResourceId</span></span>
<span data-ttu-id="dabe1-131">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dabe1-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabe1-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="dabe1-132">-Confirm</span></span>
<span data-ttu-id="dabe1-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dabe1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dabe1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dabe1-134">-WhatIf</span></span>
<span data-ttu-id="dabe1-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dabe1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dabe1-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dabe1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dabe1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabe1-137">CommonParameters</span></span>
<span data-ttu-id="dabe1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dabe1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabe1-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dabe1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabe1-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dabe1-140">INPUTS</span></span>

### <span data-ttu-id="dabe1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dabe1-141">System.String</span></span>

### <span data-ttu-id="dabe1-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dabe1-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="dabe1-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dabe1-143">OUTPUTS</span></span>

### <span data-ttu-id="dabe1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dabe1-144">System.Boolean</span></span>

## <span data-ttu-id="dabe1-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dabe1-145">NOTES</span></span>

## <span data-ttu-id="dabe1-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dabe1-146">RELATED LINKS</span></span>
