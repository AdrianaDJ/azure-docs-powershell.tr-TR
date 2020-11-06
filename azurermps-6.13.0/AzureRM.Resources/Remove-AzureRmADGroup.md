---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
ms.openlocfilehash: f9aa1f3d45a50a59c118abea4278bfed1725fa9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589371"
---
# <span data-ttu-id="38bc9-101">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="38bc9-101">Remove-AzureRmADGroup</span></span>

## <span data-ttu-id="38bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="38bc9-103">Active Directory grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="38bc9-103">Deletes an active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38bc9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38bc9-104">SYNTAX</span></span>

### <span data-ttu-id="38bc9-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38bc9-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bc9-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38bc9-106">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bc9-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="38bc9-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38bc9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="38bc9-108">DESCRIPTION</span></span>
<span data-ttu-id="38bc9-109">Active Directory grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="38bc9-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="38bc9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38bc9-110">EXAMPLES</span></span>

### <span data-ttu-id="38bc9-111">Örnek 1-Group By nesne kimliğini kaldırma</span><span class="sxs-lookup"><span data-stu-id="38bc9-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="38bc9-112">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268T322EEE ' olan grubu kiracıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="38bc9-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="38bc9-113">Örnek 2-bir grubu boru by ile kaldırma</span><span class="sxs-lookup"><span data-stu-id="38bc9-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroup
```

<span data-ttu-id="38bc9-114">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve kanalları kiracıya kaldırmak için Remove-AzureRmADGroup olan grubu alır.</span><span class="sxs-lookup"><span data-stu-id="38bc9-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzureRmADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="38bc9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38bc9-115">PARAMETERS</span></span>

### <span data-ttu-id="38bc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bc9-116">-DefaultProfile</span></span>
<span data-ttu-id="38bc9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38bc9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bc9-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="38bc9-118">-DisplayName</span></span>
<span data-ttu-id="38bc9-119">Kaldırılacak grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="38bc9-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="38bc9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="38bc9-120">-Force</span></span>
<span data-ttu-id="38bc9-121">Belirtilmişse, grubu silme konusunda onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="38bc9-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="38bc9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38bc9-122">-InputObject</span></span>
<span data-ttu-id="38bc9-123">Kaldırılacak grubun nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="38bc9-123">The object representation of the group to be removed.</span></span>

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

### <span data-ttu-id="38bc9-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="38bc9-124">-ObjectId</span></span>
<span data-ttu-id="38bc9-125">Kaldırılacak grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="38bc9-125">The object id of the group to be removed.</span></span>

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

### <span data-ttu-id="38bc9-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="38bc9-126">-PassThru</span></span>
<span data-ttu-id="38bc9-127">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="38bc9-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="38bc9-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="38bc9-128">-Confirm</span></span>
<span data-ttu-id="38bc9-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38bc9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38bc9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bc9-130">-WhatIf</span></span>
<span data-ttu-id="38bc9-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38bc9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38bc9-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38bc9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38bc9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bc9-133">CommonParameters</span></span>
<span data-ttu-id="38bc9-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38bc9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bc9-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38bc9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bc9-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38bc9-136">INPUTS</span></span>

### <span data-ttu-id="38bc9-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="38bc9-137">System.Guid</span></span>

### <span data-ttu-id="38bc9-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="38bc9-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="38bc9-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="38bc9-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="38bc9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38bc9-140">OUTPUTS</span></span>

### <span data-ttu-id="38bc9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38bc9-141">System.Boolean</span></span>

## <span data-ttu-id="38bc9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38bc9-142">NOTES</span></span>

## <span data-ttu-id="38bc9-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38bc9-143">RELATED LINKS</span></span>
