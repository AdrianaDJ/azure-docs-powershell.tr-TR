---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763552"
---
# <span data-ttu-id="55d0e-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="55d0e-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="55d0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="55d0e-103">İlke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="55d0e-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55d0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55d0e-104">SYNTAX</span></span>

### <span data-ttu-id="55d0e-105">Getallpolicyasya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55d0e-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="55d0e-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="55d0e-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="55d0e-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="55d0e-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="55d0e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="55d0e-108">DESCRIPTION</span></span>
<span data-ttu-id="55d0e-109">**Get-AzureRmPolicyAssignment** cmdlet 'i tüm ilke atamalarını veya belirli atamaları alır.</span><span class="sxs-lookup"><span data-stu-id="55d0e-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="55d0e-110">Ad ve kapsam veya KIMLIĞE göre alınacak bir ilke ataması belirleyin.</span><span class="sxs-lookup"><span data-stu-id="55d0e-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="55d0e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55d0e-111">EXAMPLES</span></span>

### <span data-ttu-id="55d0e-112">Örnek 1: tüm ilke atamalarını alma</span><span class="sxs-lookup"><span data-stu-id="55d0e-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="55d0e-113">Bu komut, tüm ilke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="55d0e-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="55d0e-114">Örnek 2: belirli bir ilke ataması alma</span><span class="sxs-lookup"><span data-stu-id="55d0e-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="55d0e-115">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="55d0e-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="55d0e-116">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="55d0e-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="55d0e-117">İkinci komut, $ResourceGroup **RESOURCEID** özelliğinin tanımladığı kapsam için PolicyAssignment07 adlı ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="55d0e-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="55d0e-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55d0e-118">PARAMETERS</span></span>

### <span data-ttu-id="55d0e-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="55d0e-119">-ApiVersion</span></span>
<span data-ttu-id="55d0e-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d0e-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="55d0e-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="55d0e-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d0e-122">-DefaultProfile</span></span>
<span data-ttu-id="55d0e-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="55d0e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="55d0e-124">-Id</span></span>
<span data-ttu-id="55d0e-125">Bu cmdlet 'in aldığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d0e-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="55d0e-126">-InformationAction</span></span>
<span data-ttu-id="55d0e-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d0e-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="55d0e-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="55d0e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55d0e-129">'A</span><span class="sxs-lookup"><span data-stu-id="55d0e-129">Continue</span></span>
- <span data-ttu-id="55d0e-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="55d0e-130">Ignore</span></span>
- <span data-ttu-id="55d0e-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="55d0e-131">Inquire</span></span>
- <span data-ttu-id="55d0e-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="55d0e-132">SilentlyContinue</span></span>
- <span data-ttu-id="55d0e-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="55d0e-133">Stop</span></span>
- <span data-ttu-id="55d0e-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="55d0e-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="55d0e-135">-InformationVariable</span></span>
<span data-ttu-id="55d0e-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d0e-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="55d0e-137">-Name</span></span>
<span data-ttu-id="55d0e-138">Bu cmdlet 'in aldığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d0e-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-139">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="55d0e-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="55d0e-140">Bu cmdlet 'in aldığı ilke atamalarının ilke tanımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d0e-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="55d0e-141">-Pre</span></span>
<span data-ttu-id="55d0e-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="55d0e-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-143">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="55d0e-143">-Scope</span></span>
<span data-ttu-id="55d0e-144">Bu cmdlet 'in aldığı ödev için ilkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d0e-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d0e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d0e-145">CommonParameters</span></span>
<span data-ttu-id="55d0e-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55d0e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d0e-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55d0e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d0e-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55d0e-148">INPUTS</span></span>

### <span data-ttu-id="55d0e-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55d0e-149">None</span></span>
<span data-ttu-id="55d0e-150">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="55d0e-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55d0e-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55d0e-151">OUTPUTS</span></span>

### <span data-ttu-id="55d0e-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="55d0e-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="55d0e-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55d0e-153">NOTES</span></span>

## <span data-ttu-id="55d0e-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55d0e-154">RELATED LINKS</span></span>

[<span data-ttu-id="55d0e-155">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="55d0e-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="55d0e-156">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="55d0e-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="55d0e-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="55d0e-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


