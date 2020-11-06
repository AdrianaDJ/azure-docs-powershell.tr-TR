---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 8b533f26b7fa947a185ee0be2dc5a395e77ebbbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591008"
---
# <span data-ttu-id="6d66a-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6d66a-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="6d66a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d66a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d66a-103">Kullanıcının atadığı kimliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d66a-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d66a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d66a-104">SYNTAX</span></span>

### <span data-ttu-id="6d66a-105">ResourceGroupAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d66a-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d66a-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="6d66a-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d66a-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6d66a-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d66a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d66a-108">DESCRIPTION</span></span>
<span data-ttu-id="6d66a-109">**Remove-Azurermuseratandidentity** belirtilen kullanıcının atadığı kimliği siler.</span><span class="sxs-lookup"><span data-stu-id="6d66a-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="6d66a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d66a-110">EXAMPLES</span></span>

### <span data-ttu-id="6d66a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6d66a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="6d66a-112">Bu örnek cmdlet 'i, **ID1** **PSRG**</span><span class="sxs-lookup"><span data-stu-id="6d66a-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>

<span data-ttu-id="6d66a-113">Değeri</span><span class="sxs-lookup"><span data-stu-id="6d66a-113">True</span></span>

## <span data-ttu-id="6d66a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d66a-114">PARAMETERS</span></span>

### <span data-ttu-id="6d66a-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="6d66a-115">-AsJob</span></span>
<span data-ttu-id="6d66a-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6d66a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d66a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d66a-117">-DefaultProfile</span></span>
<span data-ttu-id="6d66a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d66a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d66a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6d66a-119">-Force</span></span>
<span data-ttu-id="6d66a-120">{{Fill Force açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6d66a-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="6d66a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d66a-121">-InputObject</span></span>
<span data-ttu-id="6d66a-122">Identity nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6d66a-122">The Identity object.</span></span>

```yaml
Type: PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d66a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d66a-123">-Name</span></span>
<span data-ttu-id="6d66a-124">Kimlik adı.</span><span class="sxs-lookup"><span data-stu-id="6d66a-124">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d66a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d66a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6d66a-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6d66a-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d66a-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6d66a-127">-ResourceId</span></span>
<span data-ttu-id="6d66a-128">Kimliğin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6d66a-128">The Identity's resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d66a-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d66a-129">-Confirm</span></span>
<span data-ttu-id="6d66a-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d66a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d66a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d66a-131">-WhatIf</span></span>
<span data-ttu-id="6d66a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d66a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d66a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d66a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d66a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d66a-134">CommonParameters</span></span>
<span data-ttu-id="6d66a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d66a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d66a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d66a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d66a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d66a-137">INPUTS</span></span>

### <span data-ttu-id="6d66a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6d66a-138">System.String</span></span>

## <span data-ttu-id="6d66a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d66a-139">OUTPUTS</span></span>

### <span data-ttu-id="6d66a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d66a-140">System.Boolean</span></span>

## <span data-ttu-id="6d66a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d66a-141">NOTES</span></span>

## <span data-ttu-id="6d66a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d66a-142">RELATED LINKS</span></span>
