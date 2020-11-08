---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109799"
---
# <span data-ttu-id="6b1d4-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6b1d4-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="6b1d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1d4-103">Disk erişimi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="6b1d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b1d4-104">SYNTAX</span></span>

### <span data-ttu-id="6b1d4-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b1d4-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b1d4-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6b1d4-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b1d4-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="6b1d4-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b1d4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b1d4-108">DESCRIPTION</span></span>
<span data-ttu-id="6b1d4-109">**Remove-AzDiskAccess** cmdlet 'i, disk erişimi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="6b1d4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b1d4-110">EXAMPLES</span></span>

### <span data-ttu-id="6b1d4-111">Örnek 1: varsayılan parametre kümesini kullanarak disk erişimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6b1d4-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="6b1d4-112">Bu komut, "ResourceGroup01" kaynak grubundaki "DiskAccess01" adlı disk erişimini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6b1d4-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="6b1d4-113">Örnek 2: kaynak KIMLIĞINI kullanarak disk erişimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6b1d4-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="6b1d4-114">Bu komut, kaynak KIMLIĞIYLE disk erişimini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6b1d4-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="6b1d4-115">Örnek 3: giriş nesnesini kullanarak disk erişimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6b1d4-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="6b1d4-116">Bu komut, InputObject 'e göre disk erişimini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6b1d4-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="6b1d4-117">Örnek 4: giriş nesnesine göre disk erişimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6b1d4-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="6b1d4-118">Bu komut, InputObject 'i yönelterek disk erişimini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6b1d4-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="6b1d4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b1d4-119">PARAMETERS</span></span>

### <span data-ttu-id="6b1d4-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="6b1d4-120">-AsJob</span></span>
<span data-ttu-id="6b1d4-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6b1d4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b1d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1d4-122">-DefaultProfile</span></span>
<span data-ttu-id="6b1d4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b1d4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b1d4-124">-InputObject</span></span>
<span data-ttu-id="6b1d4-125">PowerShell disk erişimi nesnesi</span><span class="sxs-lookup"><span data-stu-id="6b1d4-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1d4-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b1d4-126">-Name</span></span>
<span data-ttu-id="6b1d4-127">Disk erişiminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1d4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b1d4-128">-ResourceGroupName</span></span>
<span data-ttu-id="6b1d4-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1d4-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6b1d4-130">-ResourceId</span></span>
<span data-ttu-id="6b1d4-131">Disk erişiminizin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1d4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b1d4-132">-Confirm</span></span>
<span data-ttu-id="6b1d4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b1d4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b1d4-134">-WhatIf</span></span>
<span data-ttu-id="6b1d4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b1d4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b1d4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1d4-137">CommonParameters</span></span>
<span data-ttu-id="6b1d4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1d4-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b1d4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1d4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b1d4-140">INPUTS</span></span>

### <span data-ttu-id="6b1d4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6b1d4-141">System.String</span></span>

### <span data-ttu-id="6b1d4-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDısaccess</span><span class="sxs-lookup"><span data-stu-id="6b1d4-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="6b1d4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b1d4-143">OUTPUTS</span></span>

### <span data-ttu-id="6b1d4-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="6b1d4-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6b1d4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b1d4-145">NOTES</span></span>

## <span data-ttu-id="6b1d4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b1d4-146">RELATED LINKS</span></span>
