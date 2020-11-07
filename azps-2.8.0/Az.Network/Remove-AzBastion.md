---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 3041e69903eaac7a748aff52c83e2e994fae22f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932296"
---
# <span data-ttu-id="9b8b3-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="9b8b3-101">Remove-AzBastion</span></span>

## <span data-ttu-id="9b8b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8b3-103">Bir kaynak kaldırma</span><span class="sxs-lookup"><span data-stu-id="9b8b3-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="9b8b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b8b3-104">SYNTAX</span></span>

### <span data-ttu-id="9b8b3-105">ByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b8b3-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b8b3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b8b3-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b8b3-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9b8b3-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b8b3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b8b3-108">DESCRIPTION</span></span>
<span data-ttu-id="9b8b3-109">Bir kaynak kaldırma Example1, ResourceGroupName ve ResourceName değerlerini kullanarak bu işlemi siler.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="9b8b3-110">Example2, ardışık düzene sahip nesnesini kullanarak başlatmayı siler.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="9b8b3-111">Example3, nesnesini kullanarak başlatmayı siler.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="9b8b3-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b8b3-112">EXAMPLES</span></span>

### <span data-ttu-id="9b8b3-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9b8b3-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="9b8b3-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9b8b3-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="9b8b3-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9b8b3-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="9b8b3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b8b3-116">PARAMETERS</span></span>

### <span data-ttu-id="9b8b3-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b8b3-117">-Confirm</span></span>
<span data-ttu-id="9b8b3-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b8b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8b3-119">-DefaultProfile</span></span>
<span data-ttu-id="9b8b3-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b8b3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9b8b3-121">-Force</span></span>
<span data-ttu-id="9b8b3-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9b8b3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b8b3-123">-InputObject</span></span>
<span data-ttu-id="9b8b3-124">Silinecek çıkarma nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8b3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b8b3-125">-Name</span></span>
<span data-ttu-id="9b8b3-126">Silinecek kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b8b3-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9b8b3-127">-PassThru</span></span>
<span data-ttu-id="9b8b3-128">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="9b8b3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b8b3-129">-ResourceGroupName</span></span>
<span data-ttu-id="9b8b3-130">Yer alan kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b8b3-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9b8b3-131">-ResourceId</span></span>
<span data-ttu-id="9b8b3-132">Silinmesi için Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8b3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b8b3-133">-WhatIf</span></span>
<span data-ttu-id="9b8b3-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b8b3-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b8b3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8b3-136">CommonParameters</span></span>
<span data-ttu-id="9b8b3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8b3-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9b8b3-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8b3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b8b3-139">INPUTS</span></span>

### <span data-ttu-id="9b8b3-140">Microsoft. Azure. Commands. Network. modeller. Pstion</span><span class="sxs-lookup"><span data-stu-id="9b8b3-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="9b8b3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9b8b3-141">System.String</span></span>

## <span data-ttu-id="9b8b3-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b8b3-142">OUTPUTS</span></span>

### <span data-ttu-id="9b8b3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b8b3-143">System.Boolean</span></span>

## <span data-ttu-id="9b8b3-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b8b3-144">NOTES</span></span>

## <span data-ttu-id="9b8b3-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b8b3-145">RELATED LINKS</span></span>
[<span data-ttu-id="9b8b3-146">Get-azma</span><span class="sxs-lookup"><span data-stu-id="9b8b3-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="9b8b3-147">Yeni-azma</span><span class="sxs-lookup"><span data-stu-id="9b8b3-147">New-AzBastion</span></span>](./New-AzBastion.md)