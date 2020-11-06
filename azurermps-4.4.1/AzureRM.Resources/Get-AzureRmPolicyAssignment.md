---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589121"
---
# <span data-ttu-id="afeb0-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="afeb0-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="afeb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afeb0-102">SYNOPSIS</span></span>
<span data-ttu-id="afeb0-103">İlke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="afeb0-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afeb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afeb0-104">SYNTAX</span></span>

### <span data-ttu-id="afeb0-105">Tüm ilke atamalarının parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="afeb0-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="afeb0-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="afeb0-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="afeb0-107">İlke atama adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="afeb0-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="afeb0-108">İlke atama kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="afeb0-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="afeb0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="afeb0-109">DESCRIPTION</span></span>
<span data-ttu-id="afeb0-110">**Get-AzureRmPolicyAssignment** cmdlet 'i tüm ilke atamalarını veya belirli atamaları alır.</span><span class="sxs-lookup"><span data-stu-id="afeb0-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="afeb0-111">Ad ve kapsam veya KIMLIĞE göre alınacak bir ilke ataması belirleyin.</span><span class="sxs-lookup"><span data-stu-id="afeb0-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="afeb0-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afeb0-112">EXAMPLES</span></span>

### <span data-ttu-id="afeb0-113">Örnek 1: tüm ilke atamalarını alma</span><span class="sxs-lookup"><span data-stu-id="afeb0-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="afeb0-114">Bu komut, tüm ilke atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="afeb0-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="afeb0-115">Örnek 2: belirli bir ilke ataması alma</span><span class="sxs-lookup"><span data-stu-id="afeb0-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="afeb0-116">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="afeb0-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="afeb0-117">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="afeb0-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="afeb0-118">İkinci komut, $ResourceGroup **RESOURCEID** özelliğinin tanımladığı kapsam için PolicyAssignment07 adlı ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="afeb0-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="afeb0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afeb0-119">PARAMETERS</span></span>

### <span data-ttu-id="afeb0-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="afeb0-120">-ApiVersion</span></span>
<span data-ttu-id="afeb0-121">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="afeb0-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="afeb0-122">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="afeb0-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="afeb0-123">-ID</span><span class="sxs-lookup"><span data-stu-id="afeb0-123">-Id</span></span>
<span data-ttu-id="afeb0-124">Bu cmdlet 'in aldığı ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="afeb0-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afeb0-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="afeb0-125">-InformationAction</span></span>
<span data-ttu-id="afeb0-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="afeb0-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="afeb0-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="afeb0-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afeb0-128">'A</span><span class="sxs-lookup"><span data-stu-id="afeb0-128">Continue</span></span>
- <span data-ttu-id="afeb0-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="afeb0-129">Ignore</span></span>
- <span data-ttu-id="afeb0-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="afeb0-130">Inquire</span></span>
- <span data-ttu-id="afeb0-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="afeb0-131">SilentlyContinue</span></span>
- <span data-ttu-id="afeb0-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="afeb0-132">Stop</span></span>
- <span data-ttu-id="afeb0-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="afeb0-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afeb0-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="afeb0-134">-InformationVariable</span></span>
<span data-ttu-id="afeb0-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="afeb0-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afeb0-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="afeb0-136">-Name</span></span>
<span data-ttu-id="afeb0-137">Bu cmdlet 'in aldığı ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afeb0-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afeb0-138">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="afeb0-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="afeb0-139">Bu cmdlet 'in aldığı ilke atamalarının ilke tanımının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="afeb0-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afeb0-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="afeb0-140">-Pre</span></span>
<span data-ttu-id="afeb0-141">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="afeb0-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="afeb0-142">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="afeb0-142">-Scope</span></span>
<span data-ttu-id="afeb0-143">Bu cmdlet 'in aldığı ödev için ilkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="afeb0-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afeb0-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afeb0-144">-DefaultProfile</span></span>
<span data-ttu-id="afeb0-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afeb0-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afeb0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afeb0-146">CommonParameters</span></span>
<span data-ttu-id="afeb0-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afeb0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afeb0-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afeb0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afeb0-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afeb0-149">INPUTS</span></span>

## <span data-ttu-id="afeb0-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afeb0-150">OUTPUTS</span></span>

### <span data-ttu-id="afeb0-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="afeb0-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="afeb0-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afeb0-152">NOTES</span></span>

## <span data-ttu-id="afeb0-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afeb0-153">RELATED LINKS</span></span>

[<span data-ttu-id="afeb0-154">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="afeb0-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="afeb0-155">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="afeb0-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="afeb0-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="afeb0-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


