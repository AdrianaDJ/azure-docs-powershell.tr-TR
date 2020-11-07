---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f2328ba75a0142a61238665eef41e32bf1fbba6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937466"
---
# <span data-ttu-id="4f1df-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="4f1df-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="4f1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f1df-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1df-103">Kayıt atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="4f1df-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="4f1df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f1df-104">SYNTAX</span></span>

### <span data-ttu-id="4f1df-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f1df-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [[-Scope] <String>] -Id <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f1df-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4f1df-106">ByResourceId</span></span>
```
Remove-AzManagedServicesAssignment -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f1df-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4f1df-107">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f1df-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f1df-108">DESCRIPTION</span></span>
<span data-ttu-id="4f1df-109">Kayıt atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="4f1df-109">Deletes a registration assignment.</span></span>

## <span data-ttu-id="4f1df-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f1df-110">EXAMPLES</span></span>

### <span data-ttu-id="4f1df-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f1df-111">Example 1</span></span>
```powershell
PS C:\Remove-AzManagedServicesAssignment -Id b037e73c-815e-4472-868f-59e51b49b949

Name                                 RegistrationDefinitionId
----                                 ------------------------
b037e73c-815e-4472-868f-59e51b49b949 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/be2f72e6-93e0-4d3f-ac50-9a756ed4ffa7
```

<span data-ttu-id="4f1df-112">Varsayılan kapsam altındaki kayıt atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="4f1df-112">Deletes the registration assignment under the default scope.</span></span>

### <span data-ttu-id="4f1df-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4f1df-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesAssignment -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/88ba878b-9a3c-40c3-80da-015cbe488a2f

Name                                 RegistrationDefinitionId
----                                 ------------------------
88ba878b-9a3c-40c3-80da-015cbe488a2f /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/40be0299-6573-4391-be2f-b41dd4aaf4f9
```

<span data-ttu-id="4f1df-114">Tam nitelikli kaynak kimliği için kayıt atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="4f1df-114">Deletes the registration assignment given the fully qualified resource id.</span></span>

### <span data-ttu-id="4f1df-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="4f1df-115">Example 3</span></span>
```powershell
PS C:\> $assignment = New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/33974646-9bce-461d-89eb-331f20fca33c
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
```

<span data-ttu-id="4f1df-116">Sağlanan giriş nesnesini kullanarak kayıt atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="4f1df-116">Deletes the registration assignment using the input object provided.</span></span>

## <span data-ttu-id="4f1df-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f1df-117">PARAMETERS</span></span>

### <span data-ttu-id="4f1df-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="4f1df-118">-AsJob</span></span>
<span data-ttu-id="4f1df-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4f1df-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f1df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1df-120">-DefaultProfile</span></span>
<span data-ttu-id="4f1df-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f1df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f1df-122">-ID</span><span class="sxs-lookup"><span data-stu-id="4f1df-122">-Id</span></span>
<span data-ttu-id="4f1df-123">Kayıt atama GUID 'SI (örneğin, b0c052e5-c437-4771-A476-8b1201158a57)</span><span class="sxs-lookup"><span data-stu-id="4f1df-123">The registration assignment GUID (for example, b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
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

### <span data-ttu-id="4f1df-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f1df-124">-InputObject</span></span>
<span data-ttu-id="4f1df-125">Kayıt atama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4f1df-125">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f1df-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4f1df-126">-ResourceId</span></span>
<span data-ttu-id="4f1df-127">Kayıt atamasının tam kaynak kimliği (örneğin,/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="4f1df-127">The fully qualified resource id of the registration assignment (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

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

### <span data-ttu-id="4f1df-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="4f1df-128">-Scope</span></span>
<span data-ttu-id="4f1df-129">Kayıt atamasının oluşturulması gereken kapsam.</span><span class="sxs-lookup"><span data-stu-id="4f1df-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f1df-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f1df-130">-Confirm</span></span>
<span data-ttu-id="4f1df-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f1df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f1df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f1df-132">-WhatIf</span></span>
<span data-ttu-id="4f1df-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f1df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f1df-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f1df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f1df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1df-135">CommonParameters</span></span>
<span data-ttu-id="4f1df-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f1df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1df-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4f1df-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1df-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f1df-138">INPUTS</span></span>

### <span data-ttu-id="4f1df-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4f1df-139">System.String</span></span>

### <span data-ttu-id="4f1df-140">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. Psregistrationödev</span><span class="sxs-lookup"><span data-stu-id="4f1df-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="4f1df-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f1df-141">OUTPUTS</span></span>

### <span data-ttu-id="4f1df-142">Microsoft. Azure. PowerShell. cmdlet. ManagedServices. modeller. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="4f1df-142">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="4f1df-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f1df-143">NOTES</span></span>

## <span data-ttu-id="4f1df-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f1df-144">RELATED LINKS</span></span>
