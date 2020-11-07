---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917596"
---
# <span data-ttu-id="a9405-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a9405-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="a9405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9405-102">SYNOPSIS</span></span>
<span data-ttu-id="a9405-103">Var olan bir şeması atamasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="a9405-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="a9405-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9405-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9405-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9405-105">DESCRIPTION</span></span>
<span data-ttu-id="a9405-106">Var olan bir şeması atamasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="a9405-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="a9405-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9405-107">EXAMPLES</span></span>

### <span data-ttu-id="a9405-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9405-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="a9405-109">Belirtilen abonelikteki şeması tanımının var olan bir ifade yazdırma atamasını güncelleyin `$blueprintObject` , parametreleri güncelleştiriyor.</span><span class="sxs-lookup"><span data-stu-id="a9405-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="a9405-110">Sistem tarafından atanan kimliği kullanır.</span><span class="sxs-lookup"><span data-stu-id="a9405-110">Uses system-assigned identity.</span></span> <span data-ttu-id="a9405-111">Konum, yönetilen kimlik oluşturmak için bölgeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a9405-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="a9405-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9405-112">PARAMETERS</span></span>

### <span data-ttu-id="a9405-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="a9405-113">-Blueprint</span></span>
<span data-ttu-id="a9405-114">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a9405-114">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9405-115">-DefaultProfile</span></span>
<span data-ttu-id="a9405-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9405-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9405-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="a9405-117">-Location</span></span>
<span data-ttu-id="a9405-118">Yönetilen kimliğin içinde oluşturulacak bölge.</span><span class="sxs-lookup"><span data-stu-id="a9405-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="a9405-119">Aka.ms/blueprintmsi adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="a9405-119">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-120">-Kilit</span><span class="sxs-lookup"><span data-stu-id="a9405-120">-Lock</span></span>
<span data-ttu-id="a9405-121">Kaynakları kilitleme.</span><span class="sxs-lookup"><span data-stu-id="a9405-121">Lock resources.</span></span>
<span data-ttu-id="a9405-122">Aka.ms/blueprintlocks adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="a9405-122">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9405-123">-Name</span></span>
<span data-ttu-id="a9405-124">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="a9405-124">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-125">-Parametre</span><span class="sxs-lookup"><span data-stu-id="a9405-125">-Parameter</span></span>
<span data-ttu-id="a9405-126">Yapıt parametresi.</span><span class="sxs-lookup"><span data-stu-id="a9405-126">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="a9405-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="a9405-128">{{Fill Resourcegroupparametre açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="a9405-128">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="a9405-129">-SecureStringParameter</span></span>
<span data-ttu-id="a9405-130">Anahtar Kasası kaynak kimliği, adı ve sürümü için güvenli dize parametresi.</span><span class="sxs-lookup"><span data-stu-id="a9405-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a9405-131">-SubscriptionId</span></span>
<span data-ttu-id="a9405-132">Blueprint atamak için SubscriptionID.</span><span class="sxs-lookup"><span data-stu-id="a9405-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="a9405-133">Virgülle ayrılmış bir SubscriptionID dizesi listesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="a9405-133">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a9405-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="a9405-135">Yapıların dağıtımını yapmak için sistem tarafından atanan kimlik.</span><span class="sxs-lookup"><span data-stu-id="a9405-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="a9405-136">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="a9405-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="a9405-137">Yapıtları dağıtmak için Kullanıcı tarafından atanan kimlik (MSI).</span><span class="sxs-lookup"><span data-stu-id="a9405-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9405-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9405-138">-Confirm</span></span>
<span data-ttu-id="a9405-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9405-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9405-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9405-140">-WhatIf</span></span>
<span data-ttu-id="a9405-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9405-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9405-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9405-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9405-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9405-143">CommonParameters</span></span>
<span data-ttu-id="a9405-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9405-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9405-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9405-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9405-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9405-146">INPUTS</span></span>

### <span data-ttu-id="a9405-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a9405-147">System.String</span></span>

### <span data-ttu-id="a9405-148">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="a9405-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a9405-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="a9405-149">System.String[]</span></span>

### <span data-ttu-id="a9405-150">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9405-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a9405-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9405-151">OUTPUTS</span></span>

### <span data-ttu-id="a9405-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="a9405-152">System.Object</span></span>
## <span data-ttu-id="a9405-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9405-153">NOTES</span></span>

## <span data-ttu-id="a9405-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9405-154">RELATED LINKS</span></span>
