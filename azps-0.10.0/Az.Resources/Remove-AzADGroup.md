---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 4d285471632c9c4bc952b2dcdc0e4ce5147fac12
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936374"
---
# <span data-ttu-id="f3c2a-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="f3c2a-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="f3c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c2a-103">Active Directory grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="f3c2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3c2a-104">SYNTAX</span></span>

### <span data-ttu-id="f3c2a-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f3c2a-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c2a-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3c2a-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c2a-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="f3c2a-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3c2a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3c2a-108">DESCRIPTION</span></span>
<span data-ttu-id="f3c2a-109">Active Directory grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="f3c2a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3c2a-110">EXAMPLES</span></span>

### <span data-ttu-id="f3c2a-111">Örnek 1-Group By nesne kimliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3c2a-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f3c2a-112">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268T322EEE ' olan grubu kiracıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="f3c2a-113">Örnek 2-bir grubu boru by ile kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3c2a-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="f3c2a-114">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve kanalları kiracıya kaldırmak için Remove-AzADGroup olan grubu alır.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="f3c2a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3c2a-115">PARAMETERS</span></span>

### <span data-ttu-id="f3c2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c2a-116">-DefaultProfile</span></span>
<span data-ttu-id="f3c2a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c2a-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3c2a-118">-DisplayName</span></span>
<span data-ttu-id="f3c2a-119">Kaldırılacak grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="f3c2a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f3c2a-120">-Force</span></span>
<span data-ttu-id="f3c2a-121">Belirtilmişse, grubu silme konusunda onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c2a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3c2a-122">-InputObject</span></span>
<span data-ttu-id="f3c2a-123">Kaldırılacak grubun nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c2a-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="f3c2a-124">-ObjectId</span></span>
<span data-ttu-id="f3c2a-125">Kaldırılacak grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c2a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f3c2a-126">-PassThru</span></span>
<span data-ttu-id="f3c2a-127">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c2a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3c2a-128">-Confirm</span></span>
<span data-ttu-id="f3c2a-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c2a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c2a-130">-WhatIf</span></span>
<span data-ttu-id="f3c2a-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3c2a-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c2a-133">CommonParameters</span></span>
<span data-ttu-id="f3c2a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3c2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c2a-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c2a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c2a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3c2a-136">INPUTS</span></span>

### <span data-ttu-id="f3c2a-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="f3c2a-137">System.Guid</span></span>

### <span data-ttu-id="f3c2a-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f3c2a-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="f3c2a-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3c2a-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f3c2a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3c2a-140">OUTPUTS</span></span>

### <span data-ttu-id="f3c2a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c2a-141">System.Boolean</span></span>

## <span data-ttu-id="f3c2a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3c2a-142">NOTES</span></span>

## <span data-ttu-id="f3c2a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3c2a-143">RELATED LINKS</span></span>
