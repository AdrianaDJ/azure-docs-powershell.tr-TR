---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: df1d25f2d5362a81bd33b74bad223bbfb952daa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753106"
---
# <span data-ttu-id="6c575-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="6c575-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="6c575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c575-102">SYNOPSIS</span></span>
<span data-ttu-id="6c575-103">Var olan bir şeması atamasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6c575-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="6c575-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c575-104">SYNTAX</span></span>

### <span data-ttu-id="6c575-105">UpdateBlueprintAssignment (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6c575-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c575-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="6c575-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c575-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c575-107">DESCRIPTION</span></span>
<span data-ttu-id="6c575-108">Var olan bir şeması atamasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6c575-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="6c575-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c575-109">EXAMPLES</span></span>

### <span data-ttu-id="6c575-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6c575-110">Example 1</span></span>
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

<span data-ttu-id="6c575-111">Belirtilen abonelikteki şeması tanımının var olan bir ifade yazdırma atamasını güncelleyin `$blueprintObject` , parametreleri güncelleştiriyor.</span><span class="sxs-lookup"><span data-stu-id="6c575-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="6c575-112">Sistem tarafından atanan kimliği kullanır.</span><span class="sxs-lookup"><span data-stu-id="6c575-112">Uses system-assigned identity.</span></span> <span data-ttu-id="6c575-113">Konum, yönetilen kimlik oluşturmak için bölgeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6c575-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="6c575-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6c575-114">Example 2</span></span>
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

<span data-ttu-id="6c575-115">Varolan bir grafik atama atamasını atama dosyası aracılığıyla güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6c575-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="6c575-116">Atama dosyasının biçimi istek/yanıt örneklerinde bulunabilir: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="6c575-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="6c575-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c575-117">PARAMETERS</span></span>

### <span data-ttu-id="6c575-118">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="6c575-118">-Blueprint</span></span>
<span data-ttu-id="6c575-119">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6c575-119">Blueprint object.</span></span>

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

### <span data-ttu-id="6c575-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c575-120">-DefaultProfile</span></span>
<span data-ttu-id="6c575-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c575-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c575-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="6c575-122">-Location</span></span>
<span data-ttu-id="6c575-123">Yönetilen kimliğin içinde oluşturulacak bölge.</span><span class="sxs-lookup"><span data-stu-id="6c575-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="6c575-124">Aka.ms/blueprintmsi adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="6c575-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="6c575-125">-Kilit</span><span class="sxs-lookup"><span data-stu-id="6c575-125">-Lock</span></span>
<span data-ttu-id="6c575-126">Kaynakları kilitleme.</span><span class="sxs-lookup"><span data-stu-id="6c575-126">Lock resources.</span></span>
<span data-ttu-id="6c575-127">Aka.ms/blueprintlocks adresinde daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="6c575-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="6c575-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c575-128">-Name</span></span>
<span data-ttu-id="6c575-129">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="6c575-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="6c575-130">-Parametre</span><span class="sxs-lookup"><span data-stu-id="6c575-130">-Parameter</span></span>
<span data-ttu-id="6c575-131">Yapıt parametresi.</span><span class="sxs-lookup"><span data-stu-id="6c575-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="6c575-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="6c575-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="6c575-133">{{Fill Resourcegroupparametre açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6c575-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="6c575-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="6c575-134">-SecureStringParameter</span></span>
<span data-ttu-id="6c575-135">Anahtar Kasası kaynak kimliği, adı ve sürümü için güvenli dize parametresi.</span><span class="sxs-lookup"><span data-stu-id="6c575-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="6c575-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6c575-136">-SubscriptionId</span></span>
<span data-ttu-id="6c575-137">Blueprint atamak için SubscriptionID.</span><span class="sxs-lookup"><span data-stu-id="6c575-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="6c575-138">Virgülle ayrılmış bir SubscriptionID dizesi listesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="6c575-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="6c575-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6c575-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="6c575-140">Yapıların dağıtımını yapmak için sistem tarafından atanan kimlik.</span><span class="sxs-lookup"><span data-stu-id="6c575-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="6c575-141">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="6c575-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="6c575-142">Yapıtları dağıtmak için Kullanıcı tarafından atanan kimlik (MSI).</span><span class="sxs-lookup"><span data-stu-id="6c575-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="6c575-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c575-143">-Confirm</span></span>
<span data-ttu-id="6c575-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c575-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c575-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c575-145">-WhatIf</span></span>
<span data-ttu-id="6c575-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c575-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c575-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c575-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c575-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c575-148">CommonParameters</span></span>
<span data-ttu-id="6c575-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c575-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c575-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c575-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c575-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c575-151">INPUTS</span></span>

### <span data-ttu-id="6c575-152">System. String</span><span class="sxs-lookup"><span data-stu-id="6c575-152">System.String</span></span>

### <span data-ttu-id="6c575-153">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="6c575-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="6c575-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="6c575-154">System.String[]</span></span>

### <span data-ttu-id="6c575-155">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c575-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c575-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c575-156">OUTPUTS</span></span>

### <span data-ttu-id="6c575-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="6c575-157">System.Object</span></span>
## <span data-ttu-id="6c575-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c575-158">NOTES</span></span>

## <span data-ttu-id="6c575-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c575-159">RELATED LINKS</span></span>
