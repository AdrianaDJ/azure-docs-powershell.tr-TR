---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268690"
---
# <span data-ttu-id="b6f95-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6f95-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="b6f95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f95-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f95-103">Bir cihazın kenar depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b6f95-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="b6f95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6f95-104">SYNTAX</span></span>

### <span data-ttu-id="b6f95-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6f95-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f95-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b6f95-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f95-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6f95-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f95-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6f95-108">DESCRIPTION</span></span>
<span data-ttu-id="b6f95-109">**Remove-AzStackEdgeStorageAccount** cmdlet 'i, bir yığın uç aygıtının Ilişkili Edge depolama hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b6f95-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="b6f95-110">Cmdlet 'teki bir parametre olarak kaldırılacak Edge depolama hesabının adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6f95-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="b6f95-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6f95-111">EXAMPLES</span></span>

### <span data-ttu-id="b6f95-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b6f95-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="b6f95-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6f95-113">PARAMETERS</span></span>

### <span data-ttu-id="b6f95-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b6f95-114">-AsJob</span></span>
<span data-ttu-id="b6f95-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b6f95-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6f95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f95-116">-DefaultProfile</span></span>
<span data-ttu-id="b6f95-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6f95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f95-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="b6f95-118">-DeviceName</span></span>
<span data-ttu-id="b6f95-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="b6f95-119">Device Name</span></span>

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

### <span data-ttu-id="b6f95-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6f95-120">-InputObject</span></span>
<span data-ttu-id="b6f95-121">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="b6f95-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f95-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6f95-122">-Name</span></span>
<span data-ttu-id="b6f95-123">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="b6f95-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f95-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b6f95-124">-PassThru</span></span>
<span data-ttu-id="b6f95-125">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="b6f95-125">returns true if successful</span></span>

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

### <span data-ttu-id="b6f95-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f95-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6f95-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b6f95-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b6f95-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b6f95-128">-ResourceId</span></span>
<span data-ttu-id="b6f95-129">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b6f95-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="b6f95-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6f95-130">-Confirm</span></span>
<span data-ttu-id="b6f95-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6f95-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f95-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f95-132">-WhatIf</span></span>
<span data-ttu-id="b6f95-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6f95-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6f95-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6f95-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f95-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f95-135">CommonParameters</span></span>
<span data-ttu-id="b6f95-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6f95-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f95-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6f95-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f95-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6f95-138">INPUTS</span></span>

### <span data-ttu-id="b6f95-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b6f95-139">System.String</span></span>

### <span data-ttu-id="b6f95-140">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6f95-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="b6f95-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6f95-141">OUTPUTS</span></span>

### <span data-ttu-id="b6f95-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6f95-142">System.Boolean</span></span>

## <span data-ttu-id="b6f95-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6f95-143">NOTES</span></span>

## <span data-ttu-id="b6f95-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6f95-144">RELATED LINKS</span></span>
