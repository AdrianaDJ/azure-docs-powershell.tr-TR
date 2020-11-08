---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 72c57f8310aaffdbe3c4afa38564c10132539749
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096114"
---
# <span data-ttu-id="fb1d7-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="fb1d7-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="fb1d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb1d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1d7-103">Aboneliğe bir şeması tanımı atayın.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="fb1d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb1d7-104">SYNTAX</span></span>

### <span data-ttu-id="fb1d7-105">CreateBlueprintAssignment (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb1d7-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb1d7-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="fb1d7-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb1d7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb1d7-107">DESCRIPTION</span></span>
<span data-ttu-id="fb1d7-108">Aboneliğe bir şeması tanımı atayın.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="fb1d7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb1d7-109">EXAMPLES</span></span>

### <span data-ttu-id="fb1d7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb1d7-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="fb1d7-111">`$blueprintObject`Tanımlı parametre ve kaynak grubu sözlüğünü kullanarak belirtilen aboneliğin şeması tanımının yeni bir şeması atamasını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="fb1d7-112">Sistem tarafından atanan kimliği kullanır.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-112">Uses system-assigned identity.</span></span> <span data-ttu-id="fb1d7-113">Konum, yönetilen kimlik oluşturmak için bölgeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="fb1d7-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fb1d7-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="fb1d7-115">`$blueprintObject`Tanımlı parametre ve kaynak grubu sözlüğünü kullanarak ve kaynak kilitlemeyi **allresources** ile yapılandırarak, belirtilen abonelik için yeni bir şeması tanımı ataması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="fb1d7-116">Varsayılan olarak sistem tarafından atanan kimliği kullanın.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="fb1d7-117">Konum, yönetilen kimlik oluşturmak için bölgeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="fb1d7-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="fb1d7-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="fb1d7-119">Belirtilen `$blueprintObject` Kullanıcı tarafından atanan kimlik kimliğini kullanarak tanımlanan parametre ve kaynak grubu sözlüğünü kullanarak belirtilen abonelikteki şeması tanımının yeni bir şeması atamasını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="fb1d7-120">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="fb1d7-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="fb1d7-121">Ödev dosyası aracılığıyla bir şeması ataması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="fb1d7-122">Atama dosyasının biçimi istek/yanıt örneklerinde bulunabilir: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="fb1d7-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="fb1d7-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb1d7-123">PARAMETERS</span></span>

### <span data-ttu-id="fb1d7-124">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="fb1d7-124">-Blueprint</span></span>
<span data-ttu-id="fb1d7-125">Blueprint tanım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-125">Blueprint definition object.</span></span>

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

### <span data-ttu-id="fb1d7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1d7-126">-DefaultProfile</span></span>
<span data-ttu-id="fb1d7-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb1d7-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="fb1d7-128">-Location</span></span>
<span data-ttu-id="fb1d7-129">Yönetilen kimliğin içinde oluşturulacak bölge.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="fb1d7-130">Aka.ms/blueprintmsi adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="fb1d7-130">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="fb1d7-131">-Kilit</span><span class="sxs-lookup"><span data-stu-id="fb1d7-131">-Lock</span></span>
<span data-ttu-id="fb1d7-132">Kaynakları kilitleme.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-132">Lock resources.</span></span>
<span data-ttu-id="fb1d7-133">Aka.ms/blueprintlocks adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="fb1d7-133">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="fb1d7-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb1d7-134">-Name</span></span>
<span data-ttu-id="fb1d7-135">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="fb1d7-136">-Parametre</span><span class="sxs-lookup"><span data-stu-id="fb1d7-136">-Parameter</span></span>
<span data-ttu-id="fb1d7-137">Yapıt parametreleri.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-137">Artifact parameters.</span></span>

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

### <span data-ttu-id="fb1d7-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="fb1d7-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="fb1d7-139">{{Fill Resourcegroupparametre açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="fb1d7-139">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="fb1d7-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="fb1d7-140">-SecureStringParameter</span></span>
<span data-ttu-id="fb1d7-141">Anahtar Kasası kaynak kimliği, adı ve sürümü için güvenli dize parametresi.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="fb1d7-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="fb1d7-142">-SubscriptionId</span></span>
<span data-ttu-id="fb1d7-143">Şeması tanımını atamak için abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="fb1d7-144">Virgülle ayrılmış bir SubscriptionID dizesi listesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="fb1d7-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fb1d7-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="fb1d7-146">Yapıların dağıtımını yapmak için sistem tarafından atanan kimlik.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="fb1d7-147">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="fb1d7-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="fb1d7-148">Yapıtları dağıtmak için Kullanıcı tarafından atanan kimlik (MSI).</span><span class="sxs-lookup"><span data-stu-id="fb1d7-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="fb1d7-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb1d7-149">-Confirm</span></span>
<span data-ttu-id="fb1d7-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb1d7-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb1d7-151">-WhatIf</span></span>
<span data-ttu-id="fb1d7-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb1d7-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb1d7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1d7-154">CommonParameters</span></span>
<span data-ttu-id="fb1d7-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb1d7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1d7-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb1d7-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1d7-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb1d7-157">INPUTS</span></span>

### <span data-ttu-id="fb1d7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="fb1d7-158">System.String</span></span>

### <span data-ttu-id="fb1d7-159">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="fb1d7-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="fb1d7-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="fb1d7-160">System.String[]</span></span>

### <span data-ttu-id="fb1d7-161">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb1d7-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fb1d7-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb1d7-162">OUTPUTS</span></span>

### <span data-ttu-id="fb1d7-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="fb1d7-163">System.Object</span></span>
## <span data-ttu-id="fb1d7-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb1d7-164">NOTES</span></span>

## <span data-ttu-id="fb1d7-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb1d7-165">RELATED LINKS</span></span>
