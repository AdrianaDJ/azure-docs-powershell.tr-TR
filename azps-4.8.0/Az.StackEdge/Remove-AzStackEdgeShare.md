---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273817"
---
# <span data-ttu-id="a88f8-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a88f8-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="a88f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a88f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a88f8-103">Cihazdan bir paylaşımı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a88f8-103">Removes a share from the device.</span></span>

## <span data-ttu-id="a88f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a88f8-104">SYNTAX</span></span>

### <span data-ttu-id="a88f8-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a88f8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a88f8-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a88f8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a88f8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a88f8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a88f8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a88f8-108">DESCRIPTION</span></span>
<span data-ttu-id="a88f8-109">**Remove-Azstackedgeedgesshares** cmdlet 'ı, yığın uç aygıtının ilişkili kenar paylaşımlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a88f8-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="a88f8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a88f8-110">EXAMPLES</span></span>

### <span data-ttu-id="a88f8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a88f8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="a88f8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a88f8-112">PARAMETERS</span></span>

### <span data-ttu-id="a88f8-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a88f8-113">-AsJob</span></span>
<span data-ttu-id="a88f8-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a88f8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a88f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a88f8-115">-DefaultProfile</span></span>
<span data-ttu-id="a88f8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a88f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a88f8-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="a88f8-117">-DeviceName</span></span>
<span data-ttu-id="a88f8-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="a88f8-118">Device Name</span></span>

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

### <span data-ttu-id="a88f8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a88f8-119">-InputObject</span></span>
<span data-ttu-id="a88f8-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="a88f8-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a88f8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a88f8-121">-Name</span></span>
<span data-ttu-id="a88f8-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="a88f8-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a88f8-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a88f8-123">-PassThru</span></span>
<span data-ttu-id="a88f8-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="a88f8-124">returns true if successful</span></span>

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

### <span data-ttu-id="a88f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a88f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="a88f8-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a88f8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a88f8-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a88f8-127">-ResourceId</span></span>
<span data-ttu-id="a88f8-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a88f8-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="a88f8-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a88f8-129">-Confirm</span></span>
<span data-ttu-id="a88f8-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a88f8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a88f8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a88f8-131">-WhatIf</span></span>
<span data-ttu-id="a88f8-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a88f8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a88f8-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a88f8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a88f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a88f8-134">CommonParameters</span></span>
<span data-ttu-id="a88f8-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a88f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a88f8-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a88f8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a88f8-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a88f8-137">INPUTS</span></span>

### <span data-ttu-id="a88f8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a88f8-138">System.String</span></span>

### <span data-ttu-id="a88f8-139">Microsoft. Azure. PowerShell. cmdlet. yığın</span><span class="sxs-lookup"><span data-stu-id="a88f8-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="a88f8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a88f8-140">OUTPUTS</span></span>

### <span data-ttu-id="a88f8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a88f8-141">System.Boolean</span></span>

## <span data-ttu-id="a88f8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a88f8-142">NOTES</span></span>

## <span data-ttu-id="a88f8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a88f8-143">RELATED LINKS</span></span>
