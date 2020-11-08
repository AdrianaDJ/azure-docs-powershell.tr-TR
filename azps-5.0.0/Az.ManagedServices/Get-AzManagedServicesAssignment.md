---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277340"
---
# <span data-ttu-id="348f0-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="348f0-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="348f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="348f0-102">SYNOPSIS</span></span>
<span data-ttu-id="348f0-103">Belirli bir kayıt atamasını veya kayıt atamalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="348f0-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="348f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="348f0-104">SYNTAX</span></span>

### <span data-ttu-id="348f0-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="348f0-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="348f0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="348f0-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="348f0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="348f0-107">DESCRIPTION</span></span>
<span data-ttu-id="348f0-108">Belirli bir kayıt atamasını veya kayıt atamalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="348f0-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="348f0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="348f0-109">EXAMPLES</span></span>

### <span data-ttu-id="348f0-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="348f0-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="348f0-111">Varsayılan kapsam altındaki tüm kayıt atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="348f0-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="348f0-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="348f0-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="348f0-113">Kayıt tanımı ayrıntılarıyla tüm kayıt atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="348f0-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="348f0-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="348f0-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="348f0-115">Kayıt tanımı ayrıntıları olmadan bir kayıt atamasını ada göre alır.</span><span class="sxs-lookup"><span data-stu-id="348f0-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="348f0-116">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="348f0-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="348f0-117">Kayıt tanımı ayrıntıları içeren ada göre bir kayıt ataması alır.</span><span class="sxs-lookup"><span data-stu-id="348f0-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="348f0-118">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="348f0-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="348f0-119">Verilen kapsamdaki tüm kayıt atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="348f0-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="348f0-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="348f0-120">PARAMETERS</span></span>

### <span data-ttu-id="348f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348f0-121">-DefaultProfile</span></span>
<span data-ttu-id="348f0-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="348f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="348f0-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="348f0-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="348f0-124">Kayıt tanımı ayrıntılarının eklenip eklenmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="348f0-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348f0-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="348f0-125">-Name</span></span>
<span data-ttu-id="348f0-126">Kayıt atamasının benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="348f0-126">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348f0-127">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="348f0-127">-Scope</span></span>
<span data-ttu-id="348f0-128">Kayıt atamasının oluşturulduğu kapsam.</span><span class="sxs-lookup"><span data-stu-id="348f0-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="348f0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348f0-129">CommonParameters</span></span>
<span data-ttu-id="348f0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="348f0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348f0-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="348f0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348f0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="348f0-132">INPUTS</span></span>

### <span data-ttu-id="348f0-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="348f0-133">None</span></span>
## <span data-ttu-id="348f0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="348f0-134">OUTPUTS</span></span>

### <span data-ttu-id="348f0-135">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. Psregistrationödev</span><span class="sxs-lookup"><span data-stu-id="348f0-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="348f0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="348f0-136">NOTES</span></span>

## <span data-ttu-id="348f0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="348f0-137">RELATED LINKS</span></span>
