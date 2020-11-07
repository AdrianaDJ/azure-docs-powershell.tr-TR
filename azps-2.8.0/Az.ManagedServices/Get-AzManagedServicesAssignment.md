---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 46972cf6d58106472335707dbebbf92ddb657b57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751420"
---
# <span data-ttu-id="f132f-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f132f-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="f132f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f132f-102">SYNOPSIS</span></span>
<span data-ttu-id="f132f-103">Kayıt atamalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f132f-103">Gets a list of the registration assignments.</span></span>

## <span data-ttu-id="f132f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f132f-104">SYNTAX</span></span>

### <span data-ttu-id="f132f-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f132f-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f132f-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="f132f-106">ById</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] -Id <String> [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f132f-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f132f-107">ByResourceId</span></span>
```
Get-AzManagedServicesAssignment -ResourceId <String> [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f132f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f132f-108">DESCRIPTION</span></span>
<span data-ttu-id="f132f-109">Kayıt atamalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f132f-109">Gets a list of the registration assignments.</span></span>

## <span data-ttu-id="f132f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f132f-110">EXAMPLES</span></span>

### <span data-ttu-id="f132f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f132f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedServicesAssignment

Name                                 RegistrationDefinitionId
----                                 ------------------------
f2e18995-6c79-4ab7-876e-1b1c8393d12c /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/a156aad7-f3ce-4a46-b240-246242b6bd78
ddd0d277-e120-4de1-8498-52b8f767b699 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8
```

<span data-ttu-id="f132f-112">Varsayılan kapsam altındaki tüm kayıt atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="f132f-112">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="f132f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f132f-113">Example 2</span></span>
```powershell
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments

Name                                 RegistrationDefinitionId
----                                 ------------------------
f2e18995-6c79-4ab7-876e-1b1c8393d12c /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/a156aad7-f3ce-4a46-b240-246242b6bd78
8b6d4693-efb0-4b58-ac94-625b6a321af3 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/bb2626be-3e11-442f-b0f1-9209508d4f52
ddd0d277-e120-4de1-8498-52b8f767b699 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8


PS C:\> $assignments[2].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : cae481c0-de7c-42a8-86c1-5b170861caf8
```

<span data-ttu-id="f132f-114">Kayıt tanımı ayrıntılarıyla tüm kayıt atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="f132f-114">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="f132f-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="f132f-115">Example 3</span></span>
```powershell
PS C:\> $assignmnent = Get-AzManagedServicesAssignment -Id ddd0d277-e120-4de1-8498-52b8f767b699
PS C:\> $assignmnent

Name                                 RegistrationDefinitionId
----                                 ------------------------
ddd0d277-e120-4de1-8498-52b8f767b699 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8

PS C:\> $assignmnent.Properties.RegistrationDefinition

Properties :
Plan       :
Id         :
Type       :
Name       :
```

<span data-ttu-id="f132f-116">Kayıt tanımı ayrıntıları olmadan bir kayıt atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="f132f-116">Gets a registration assignment without the registration definition details.</span></span>

### <span data-ttu-id="f132f-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="f132f-117">Example 4</span></span>
```powershell
PS C:\> $assignmnentWithDef = Get-AzManagedServicesAssignment -Id ddd0d277-e120-4de1-8498-52b8f767b699 -ExpandRegistrationDefinition
PS C:\> $assignmnentWithDef

Name                                 RegistrationDefinitionId
----                                 ------------------------
ddd0d277-e120-4de1-8498-52b8f767b699 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8


PS C:\> $assignmnentWithDef.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : cae481c0-de7c-42a8-86c1-5b170861caf8
```

<span data-ttu-id="f132f-118">Kayıt tanımı ayrıntılarını içeren bir kayıt atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="f132f-118">Gets a registration assignment with registration definition details.</span></span>

### <span data-ttu-id="f132f-119">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="f132f-119">Example 5</span></span>
```powershell
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/resourceGroups/newRG

Name                                 RegistrationDefinitionId
----                                 ------------------------
c5deb1ba-8e27-4935-8af5-9242e7dabd24 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/447b1aff-b0fc-4959-989d-d77dc93f3509
aa891268-329a-4637-b3f6-2877ea304f8b /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/46b981a7-63ff-4063-9961-9fce4ddea376
```

<span data-ttu-id="f132f-120">Tüm kayıt atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="f132f-120">Gets all the registration assignments.</span></span>

### <span data-ttu-id="f132f-121">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="f132f-121">Example 6</span></span>
```powershell
PS C:\> $assignments = Get-AzManagedServicesAssignment
PS C:\> $assignments[0].Id
/subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/f2e18995-6c79-4ab7-876e-1b1c8393d12c
PS C:\> Get-AzManagedServicesAssignment -ResourceId $assignments[0].Id

Name                                 RegistrationDefinitionId
----                                 ------------------------
f2e18995-6c79-4ab7-876e-1b1c8393d12c /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/a156aad7-f3ce-4a46-b240-246242b6bd78
```

<span data-ttu-id="f132f-122">Tam nitelikli kaynak kimliği için kayıt atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="f132f-122">Gets the registration assignment given the fully qualified resource id.</span></span>

## <span data-ttu-id="f132f-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f132f-123">PARAMETERS</span></span>

### <span data-ttu-id="f132f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f132f-124">-DefaultProfile</span></span>
<span data-ttu-id="f132f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f132f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f132f-126">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="f132f-126">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="f132f-127">Kayıt tanımı ayrıntılarının eklenip eklenmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="f132f-127">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="f132f-128">-ID</span><span class="sxs-lookup"><span data-stu-id="f132f-128">-Id</span></span>
<span data-ttu-id="f132f-129">Kayıt atama tanımlayıcısı (örneğin, b0c052e5-c437-4771-A476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="f132f-129">The Registration Assignment identifier (for example, b0c052e5-c437-4771-a476-8b1201158a57).</span></span>
```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f132f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f132f-130">-ResourceId</span></span>
<span data-ttu-id="f132f-131">Kayıt atama RESOURCEID (örneğin,/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57)</span><span class="sxs-lookup"><span data-stu-id="f132f-131">The Registration Assignment ResourceId (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f132f-132">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="f132f-132">-Scope</span></span>
<span data-ttu-id="f132f-133">Kayıt atamasının oluşturulduğu kapsam.</span><span class="sxs-lookup"><span data-stu-id="f132f-133">The scope where the registration assignment is created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f132f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f132f-134">CommonParameters</span></span>
<span data-ttu-id="f132f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f132f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f132f-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f132f-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f132f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f132f-137">INPUTS</span></span>

### <span data-ttu-id="f132f-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f132f-138">None</span></span>

## <span data-ttu-id="f132f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f132f-139">OUTPUTS</span></span>

### <span data-ttu-id="f132f-140">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. Psregistrationödev</span><span class="sxs-lookup"><span data-stu-id="f132f-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="f132f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f132f-141">NOTES</span></span>

## <span data-ttu-id="f132f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f132f-142">RELATED LINKS</span></span>
