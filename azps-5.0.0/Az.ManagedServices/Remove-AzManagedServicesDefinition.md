---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277332"
---
# <span data-ttu-id="0cce2-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0cce2-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="0cce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cce2-102">SYNOPSIS</span></span>
<span data-ttu-id="0cce2-103">Kayıt tanımını siler.</span><span class="sxs-lookup"><span data-stu-id="0cce2-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="0cce2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0cce2-104">SYNTAX</span></span>

### <span data-ttu-id="0cce2-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0cce2-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cce2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0cce2-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cce2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0cce2-107">DESCRIPTION</span></span>
<span data-ttu-id="0cce2-108">Kayıt tanımını siler.</span><span class="sxs-lookup"><span data-stu-id="0cce2-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="0cce2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0cce2-109">EXAMPLES</span></span>

### <span data-ttu-id="0cce2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0cce2-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="0cce2-111">Varsayılan kapsamda kayıt tanımını adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0cce2-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="0cce2-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0cce2-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="0cce2-113">Giriş nesnesi verilen kayıt tanımını siler.</span><span class="sxs-lookup"><span data-stu-id="0cce2-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="0cce2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0cce2-114">PARAMETERS</span></span>

### <span data-ttu-id="0cce2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cce2-115">-DefaultProfile</span></span>
<span data-ttu-id="0cce2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0cce2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cce2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cce2-117">-InputObject</span></span>
<span data-ttu-id="0cce2-118">Kayıt tanımı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0cce2-118">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cce2-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0cce2-119">-Name</span></span>
<span data-ttu-id="0cce2-120">Kayıt tanımının benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="0cce2-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cce2-121">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="0cce2-121">-Scope</span></span>
<span data-ttu-id="0cce2-122">Kayıt tanımının oluşturulduğu kapsam.</span><span class="sxs-lookup"><span data-stu-id="0cce2-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cce2-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="0cce2-123">-Confirm</span></span>
<span data-ttu-id="0cce2-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0cce2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cce2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cce2-125">-WhatIf</span></span>
<span data-ttu-id="0cce2-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0cce2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cce2-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0cce2-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cce2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cce2-128">CommonParameters</span></span>
<span data-ttu-id="0cce2-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0cce2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cce2-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0cce2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cce2-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0cce2-131">INPUTS</span></span>

### <span data-ttu-id="0cce2-132">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="0cce2-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="0cce2-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0cce2-133">OUTPUTS</span></span>

### <span data-ttu-id="0cce2-134">System. void</span><span class="sxs-lookup"><span data-stu-id="0cce2-134">System.Void</span></span>
## <span data-ttu-id="0cce2-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0cce2-135">NOTES</span></span>

## <span data-ttu-id="0cce2-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0cce2-136">RELATED LINKS</span></span>
