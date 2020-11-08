---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: d066e36b4430f865143a8e8ee14693c38054f02c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268822"
---
# <span data-ttu-id="75f16-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="75f16-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="75f16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f16-102">SYNOPSIS</span></span>
<span data-ttu-id="75f16-103">Active Directory grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="75f16-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="75f16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75f16-104">SYNTAX</span></span>

### <span data-ttu-id="75f16-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75f16-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f16-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75f16-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f16-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="75f16-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75f16-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="75f16-108">DESCRIPTION</span></span>
<span data-ttu-id="75f16-109">Active Directory grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="75f16-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="75f16-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75f16-110">EXAMPLES</span></span>

### <span data-ttu-id="75f16-111">Örnek 1: bir gruplandırma nesnesi kimliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="75f16-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="75f16-112">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268T322EEE ' olan grubu kiracıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="75f16-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="75f16-113">Örnek 2: bir grubu boru by ile kaldırma</span><span class="sxs-lookup"><span data-stu-id="75f16-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="75f16-114">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve kanalları kiracıya kaldırmak için Remove-AzADGroup olan grubu alır.</span><span class="sxs-lookup"><span data-stu-id="75f16-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="75f16-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75f16-115">PARAMETERS</span></span>

### <span data-ttu-id="75f16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f16-116">-DefaultProfile</span></span>
<span data-ttu-id="75f16-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75f16-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75f16-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75f16-118">-DisplayName</span></span>
<span data-ttu-id="75f16-119">Kaldırılacak grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="75f16-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f16-120">-Force</span><span class="sxs-lookup"><span data-stu-id="75f16-120">-Force</span></span>
<span data-ttu-id="75f16-121">Belirtilmişse, grubu silme konusunda onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="75f16-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="75f16-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75f16-122">-InputObject</span></span>
<span data-ttu-id="75f16-123">Kaldırılacak grubun nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="75f16-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75f16-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="75f16-124">-ObjectId</span></span>
<span data-ttu-id="75f16-125">Kaldırılacak grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="75f16-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f16-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="75f16-126">-PassThru</span></span>
<span data-ttu-id="75f16-127">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="75f16-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="75f16-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="75f16-128">-Confirm</span></span>
<span data-ttu-id="75f16-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75f16-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75f16-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f16-130">-WhatIf</span></span>
<span data-ttu-id="75f16-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75f16-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f16-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75f16-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75f16-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f16-133">CommonParameters</span></span>
<span data-ttu-id="75f16-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75f16-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f16-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="75f16-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f16-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75f16-136">INPUTS</span></span>

### <span data-ttu-id="75f16-137">System. String</span><span class="sxs-lookup"><span data-stu-id="75f16-137">System.String</span></span>

### <span data-ttu-id="75f16-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="75f16-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="75f16-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75f16-139">OUTPUTS</span></span>

### <span data-ttu-id="75f16-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75f16-140">System.Boolean</span></span>

## <span data-ttu-id="75f16-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75f16-141">NOTES</span></span>

## <span data-ttu-id="75f16-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75f16-142">RELATED LINKS</span></span>
