---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917592"
---
# <span data-ttu-id="ca3f9-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="ca3f9-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="ca3f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca3f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3f9-103">Aboneliğe bir şeması tanımı atayın.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="ca3f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca3f9-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca3f9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca3f9-105">DESCRIPTION</span></span>
<span data-ttu-id="ca3f9-106">Aboneliğe bir şeması tanımı atayın.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="ca3f9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca3f9-107">EXAMPLES</span></span>

### <span data-ttu-id="ca3f9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ca3f9-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="ca3f9-109">`$blueprintObject`Tanımlı parametre ve kaynak grubu sözlüğünü kullanarak belirtilen aboneliğin şeması tanımının yeni bir şeması atamasını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="ca3f9-110">Sistem tarafından atanan kimliği kullanır.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-110">Uses system-assigned identity.</span></span> <span data-ttu-id="ca3f9-111">Konum, yönetilen kimlik oluşturmak için bölgeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="ca3f9-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ca3f9-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="ca3f9-113">`$blueprintObject`Tanımlı parametre ve kaynak grubu sözlüğünü kullanarak ve kaynak kilitlemeyi **allresources** ile yapılandırarak, belirtilen abonelik için yeni bir şeması tanımı ataması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="ca3f9-114">Varsayılan olarak sistem tarafından atanan kimliği kullanın.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="ca3f9-115">Konum, yönetilen kimlik oluşturmak için bölgeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="ca3f9-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ca3f9-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="ca3f9-117">Belirtilen `$blueprintObject` Kullanıcı tarafından atanan kimlik kimliğini kullanarak tanımlanan parametre ve kaynak grubu sözlüğünü kullanarak belirtilen abonelikteki şeması tanımının yeni bir şeması atamasını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="ca3f9-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca3f9-118">PARAMETERS</span></span>

### <span data-ttu-id="ca3f9-119">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="ca3f9-119">-Blueprint</span></span>
<span data-ttu-id="ca3f9-120">Blueprint tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="ca3f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3f9-121">-DefaultProfile</span></span>
<span data-ttu-id="ca3f9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca3f9-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="ca3f9-123">-Location</span></span>
<span data-ttu-id="ca3f9-124">Yönetilen kimliğin içinde oluşturulacak bölge.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="ca3f9-125">Aka.ms/blueprintmsi adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="ca3f9-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="ca3f9-126">-Kilit</span><span class="sxs-lookup"><span data-stu-id="ca3f9-126">-Lock</span></span>
<span data-ttu-id="ca3f9-127">Kaynakları kilitleme.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-127">Lock resources.</span></span>
<span data-ttu-id="ca3f9-128">Aka.ms/blueprintlocks adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="ca3f9-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="ca3f9-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca3f9-129">-Name</span></span>
<span data-ttu-id="ca3f9-130">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="ca3f9-131">-Parametre</span><span class="sxs-lookup"><span data-stu-id="ca3f9-131">-Parameter</span></span>
<span data-ttu-id="ca3f9-132">Yapıt parametreleri.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="ca3f9-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="ca3f9-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="ca3f9-134">{{Fill Resourcegroupparametre açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ca3f9-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="ca3f9-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="ca3f9-135">-SecureStringParameter</span></span>
<span data-ttu-id="ca3f9-136">Anahtar Kasası kaynak kimliği, adı ve sürümü için güvenli dize parametresi.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="ca3f9-137">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ca3f9-137">-SubscriptionId</span></span>
<span data-ttu-id="ca3f9-138">Şeması tanımını atamak için abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="ca3f9-139">Virgülle ayrılmış bir SubscriptionID dizesi listesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="ca3f9-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ca3f9-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="ca3f9-141">Yapıların dağıtımını yapmak için sistem tarafından atanan kimlik.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="ca3f9-142">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="ca3f9-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="ca3f9-143">Yapıtları dağıtmak için Kullanıcı tarafından atanan kimlik (MSI).</span><span class="sxs-lookup"><span data-stu-id="ca3f9-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="ca3f9-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca3f9-144">-Confirm</span></span>
<span data-ttu-id="ca3f9-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca3f9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3f9-146">-WhatIf</span></span>
<span data-ttu-id="ca3f9-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca3f9-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca3f9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3f9-149">CommonParameters</span></span>
<span data-ttu-id="ca3f9-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca3f9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3f9-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca3f9-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3f9-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca3f9-152">INPUTS</span></span>

### <span data-ttu-id="ca3f9-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ca3f9-153">System.String</span></span>

### <span data-ttu-id="ca3f9-154">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="ca3f9-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="ca3f9-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="ca3f9-155">System.String[]</span></span>

### <span data-ttu-id="ca3f9-156">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca3f9-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca3f9-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca3f9-157">OUTPUTS</span></span>

### <span data-ttu-id="ca3f9-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="ca3f9-158">System.Object</span></span>
## <span data-ttu-id="ca3f9-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca3f9-159">NOTES</span></span>

## <span data-ttu-id="ca3f9-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca3f9-160">RELATED LINKS</span></span>
