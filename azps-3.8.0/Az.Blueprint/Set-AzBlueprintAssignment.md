---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 418bb8a9ba8362e799d619705eccdc60e5418fc9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096464"
---
# <span data-ttu-id="c65a3-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c65a3-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="c65a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c65a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c65a3-103">Var olan bir şeması atamasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c65a3-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="c65a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c65a3-104">SYNTAX</span></span>

### <span data-ttu-id="c65a3-105">UpdateBlueprintAssignment (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c65a3-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c65a3-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="c65a3-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c65a3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c65a3-107">DESCRIPTION</span></span>
<span data-ttu-id="c65a3-108">Var olan bir şeması atamasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c65a3-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="c65a3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c65a3-109">EXAMPLES</span></span>

### <span data-ttu-id="c65a3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c65a3-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="c65a3-111">Belirtilen abonelikteki şeması tanımının var olan bir ifade yazdırma atamasını güncelleyin `$blueprintObject` , parametreleri güncelleştiriyor.</span><span class="sxs-lookup"><span data-stu-id="c65a3-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="c65a3-112">Sistem tarafından atanan kimliği kullanır.</span><span class="sxs-lookup"><span data-stu-id="c65a3-112">Uses system-assigned identity.</span></span> <span data-ttu-id="c65a3-113">Konum, yönetilen kimlik oluşturmak için bölgeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c65a3-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="c65a3-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c65a3-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="c65a3-115">Varolan bir grafik atama atamasını atama dosyası aracılığıyla güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c65a3-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="c65a3-116">Atama dosyasının biçimi istek/yanıt örneklerinde bulunabilir: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="c65a3-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="c65a3-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c65a3-117">PARAMETERS</span></span>

### <span data-ttu-id="c65a3-118">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="c65a3-118">-Blueprint</span></span>
<span data-ttu-id="c65a3-119">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c65a3-119">Blueprint object.</span></span>

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

### <span data-ttu-id="c65a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65a3-120">-DefaultProfile</span></span>
<span data-ttu-id="c65a3-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c65a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c65a3-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="c65a3-122">-Location</span></span>
<span data-ttu-id="c65a3-123">Yönetilen kimliğin içinde oluşturulacak bölge.</span><span class="sxs-lookup"><span data-stu-id="c65a3-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="c65a3-124">Aka.ms/blueprintmsi adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="c65a3-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="c65a3-125">-Kilit</span><span class="sxs-lookup"><span data-stu-id="c65a3-125">-Lock</span></span>
<span data-ttu-id="c65a3-126">Kaynakları kilitleme.</span><span class="sxs-lookup"><span data-stu-id="c65a3-126">Lock resources.</span></span>
<span data-ttu-id="c65a3-127">Aka.ms/blueprintlocks adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="c65a3-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="c65a3-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="c65a3-128">-Name</span></span>
<span data-ttu-id="c65a3-129">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="c65a3-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="c65a3-130">-Parametre</span><span class="sxs-lookup"><span data-stu-id="c65a3-130">-Parameter</span></span>
<span data-ttu-id="c65a3-131">Yapıt parametresi.</span><span class="sxs-lookup"><span data-stu-id="c65a3-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="c65a3-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="c65a3-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="c65a3-133">{{Fill Resourcegroupparametre açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c65a3-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="c65a3-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="c65a3-134">-SecureStringParameter</span></span>
<span data-ttu-id="c65a3-135">Anahtar Kasası kaynak kimliği, adı ve sürümü için güvenli dize parametresi.</span><span class="sxs-lookup"><span data-stu-id="c65a3-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="c65a3-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c65a3-136">-SubscriptionId</span></span>
<span data-ttu-id="c65a3-137">Blueprint atamak için SubscriptionID.</span><span class="sxs-lookup"><span data-stu-id="c65a3-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="c65a3-138">Virgülle ayrılmış bir SubscriptionID dizesi listesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="c65a3-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="c65a3-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c65a3-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="c65a3-140">Yapıların dağıtımını yapmak için sistem tarafından atanan kimlik.</span><span class="sxs-lookup"><span data-stu-id="c65a3-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="c65a3-141">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="c65a3-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="c65a3-142">Yapıtları dağıtmak için Kullanıcı tarafından atanan kimlik (MSI).</span><span class="sxs-lookup"><span data-stu-id="c65a3-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="c65a3-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="c65a3-143">-Confirm</span></span>
<span data-ttu-id="c65a3-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c65a3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c65a3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c65a3-145">-WhatIf</span></span>
<span data-ttu-id="c65a3-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c65a3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c65a3-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c65a3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c65a3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65a3-148">CommonParameters</span></span>
<span data-ttu-id="c65a3-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c65a3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65a3-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65a3-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65a3-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c65a3-151">INPUTS</span></span>

### <span data-ttu-id="c65a3-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c65a3-152">System.String</span></span>

### <span data-ttu-id="c65a3-153">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c65a3-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c65a3-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="c65a3-154">System.String[]</span></span>

### <span data-ttu-id="c65a3-155">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c65a3-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c65a3-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c65a3-156">OUTPUTS</span></span>

### <span data-ttu-id="c65a3-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="c65a3-157">System.Object</span></span>
## <span data-ttu-id="c65a3-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c65a3-158">NOTES</span></span>

## <span data-ttu-id="c65a3-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c65a3-159">RELATED LINKS</span></span>
