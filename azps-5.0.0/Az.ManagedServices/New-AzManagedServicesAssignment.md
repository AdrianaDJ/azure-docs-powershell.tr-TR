---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277334"
---
# <span data-ttu-id="95638-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="95638-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="95638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95638-102">SYNOPSIS</span></span>
<span data-ttu-id="95638-103">Bir kayıt ataması oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="95638-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="95638-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95638-104">SYNTAX</span></span>

### <span data-ttu-id="95638-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95638-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95638-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="95638-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95638-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="95638-107">DESCRIPTION</span></span>
<span data-ttu-id="95638-108">Bir kayıt ataması oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="95638-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="95638-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95638-109">EXAMPLES</span></span>

### <span data-ttu-id="95638-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="95638-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="95638-111">Kayıt tanım tanımlayıcısını kullanarak varsayılan kapsamda bir kayıt ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95638-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="95638-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="95638-112">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\>
```

<span data-ttu-id="95638-113">Giriş olarak kayıt tanımı nesnesini içeren bir kayıt ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="95638-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="95638-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="95638-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="95638-115">Kayıt atamasını kayıt tanımı tanımlayıcısı ve adıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="95638-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="95638-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95638-116">PARAMETERS</span></span>

### <span data-ttu-id="95638-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95638-117">-DefaultProfile</span></span>
<span data-ttu-id="95638-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95638-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95638-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="95638-119">-Name</span></span>
<span data-ttu-id="95638-120">Kayıt atamasının benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="95638-120">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95638-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="95638-121">-RegistrationDefinition</span></span>
<span data-ttu-id="95638-122">Kayıt tanımı giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="95638-122">The registration definition input object.</span></span>

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

### <span data-ttu-id="95638-123">-Registrationdefinitionıd</span><span class="sxs-lookup"><span data-stu-id="95638-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="95638-124">Kayıt tanımının tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="95638-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95638-125">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="95638-125">-Scope</span></span>
<span data-ttu-id="95638-126">Kayıt atamasının oluşturulması gereken kapsam.</span><span class="sxs-lookup"><span data-stu-id="95638-126">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95638-127">-Iş</span><span class="sxs-lookup"><span data-stu-id="95638-127">-AsJob</span></span>
<span data-ttu-id="95638-128">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="95638-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95638-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="95638-129">-Confirm</span></span>
<span data-ttu-id="95638-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95638-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95638-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95638-131">-WhatIf</span></span>
<span data-ttu-id="95638-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95638-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95638-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95638-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95638-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95638-134">CommonParameters</span></span>
<span data-ttu-id="95638-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95638-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95638-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="95638-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95638-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95638-137">INPUTS</span></span>

### <span data-ttu-id="95638-138">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="95638-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="95638-139">System. String</span><span class="sxs-lookup"><span data-stu-id="95638-139">System.String</span></span>
## <span data-ttu-id="95638-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95638-140">OUTPUTS</span></span>

### <span data-ttu-id="95638-141">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. Psregistrationödev</span><span class="sxs-lookup"><span data-stu-id="95638-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="95638-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95638-142">NOTES</span></span>

## <span data-ttu-id="95638-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95638-143">RELATED LINKS</span></span>
