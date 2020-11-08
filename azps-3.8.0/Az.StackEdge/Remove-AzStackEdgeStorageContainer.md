---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103905"
---
# <span data-ttu-id="0164c-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0164c-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="0164c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0164c-102">SYNOPSIS</span></span>
<span data-ttu-id="0164c-103">Cihazda Edge depolama hesabı için depolama kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0164c-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="0164c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0164c-104">SYNTAX</span></span>

### <span data-ttu-id="0164c-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0164c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0164c-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0164c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0164c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0164c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0164c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0164c-108">DESCRIPTION</span></span>
<span data-ttu-id="0164c-109">**Remove-AzStackEdgeStorageContainer** cmdlet 'ı, yığın uç cihazında Edge depolama hesabı için ilişkili bir depolama kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0164c-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="0164c-110">Parametre olarak kaldırılacak depolama kapsayıcısının adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0164c-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="0164c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0164c-111">EXAMPLES</span></span>

### <span data-ttu-id="0164c-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0164c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="0164c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0164c-113">PARAMETERS</span></span>

### <span data-ttu-id="0164c-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0164c-114">-AsJob</span></span>
<span data-ttu-id="0164c-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0164c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0164c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0164c-116">-DefaultProfile</span></span>
<span data-ttu-id="0164c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0164c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0164c-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="0164c-118">-DeviceName</span></span>
<span data-ttu-id="0164c-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="0164c-119">Device Name</span></span>

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

### <span data-ttu-id="0164c-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0164c-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="0164c-121">Var olan EdgeStorageAccount adının adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="0164c-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="0164c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0164c-122">-InputObject</span></span>
<span data-ttu-id="0164c-123">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="0164c-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0164c-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="0164c-124">-Name</span></span>
<span data-ttu-id="0164c-125">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="0164c-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0164c-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0164c-126">-PassThru</span></span>
<span data-ttu-id="0164c-127">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="0164c-127">returns true if successful</span></span>

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

### <span data-ttu-id="0164c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0164c-128">-ResourceGroupName</span></span>
<span data-ttu-id="0164c-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0164c-129">Resource Group Name</span></span>

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

### <span data-ttu-id="0164c-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0164c-130">-ResourceId</span></span>
<span data-ttu-id="0164c-131">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0164c-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="0164c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0164c-132">-Confirm</span></span>
<span data-ttu-id="0164c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0164c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0164c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0164c-134">-WhatIf</span></span>
<span data-ttu-id="0164c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0164c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0164c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0164c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0164c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0164c-137">CommonParameters</span></span>
<span data-ttu-id="0164c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0164c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0164c-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0164c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0164c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0164c-140">INPUTS</span></span>

### <span data-ttu-id="0164c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0164c-141">System.String</span></span>

### <span data-ttu-id="0164c-142">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0164c-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="0164c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0164c-143">OUTPUTS</span></span>

### <span data-ttu-id="0164c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0164c-144">System.Boolean</span></span>

## <span data-ttu-id="0164c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0164c-145">NOTES</span></span>

## <span data-ttu-id="0164c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0164c-146">RELATED LINKS</span></span>
