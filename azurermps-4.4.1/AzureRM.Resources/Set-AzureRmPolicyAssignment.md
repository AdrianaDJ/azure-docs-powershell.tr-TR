---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589119"
---
# <span data-ttu-id="838d2-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="838d2-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="838d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="838d2-102">SYNOPSIS</span></span>
<span data-ttu-id="838d2-103">Bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="838d2-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="838d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="838d2-104">SYNTAX</span></span>

### <span data-ttu-id="838d2-105">İlke atama adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="838d2-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="838d2-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="838d2-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="838d2-107">İlke atama kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="838d2-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="838d2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="838d2-108">DESCRIPTION</span></span>
<span data-ttu-id="838d2-109">**Set-AzureRmPolicyAssignment** cmdlet 'i bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="838d2-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="838d2-110">KIMLIĞE göre veya ad ve kapsamla bir ödev belirtin.</span><span class="sxs-lookup"><span data-stu-id="838d2-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="838d2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="838d2-111">EXAMPLES</span></span>

### <span data-ttu-id="838d2-112">Örnek 1: görünen adı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="838d2-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="838d2-113">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="838d2-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="838d2-114">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="838d2-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="838d2-115">İkinci komut, Get-AzureRmPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="838d2-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="838d2-116">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="838d2-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="838d2-117">Son komutu, $PolicyAssignment 'un **RESOURCEID** özelliğiyle tanımlanan ilke atamasında görünen adı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="838d2-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="838d2-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="838d2-118">PARAMETERS</span></span>

### <span data-ttu-id="838d2-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="838d2-119">-ApiVersion</span></span>
<span data-ttu-id="838d2-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="838d2-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="838d2-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="838d2-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="838d2-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="838d2-122">-DisplayName</span></span>
<span data-ttu-id="838d2-123">İlke ataması için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="838d2-123">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="838d2-124">-ID</span><span class="sxs-lookup"><span data-stu-id="838d2-124">-Id</span></span>
<span data-ttu-id="838d2-125">Bu cmdlet 'in değiştirdiği ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="838d2-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="838d2-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="838d2-126">-InformationAction</span></span>
<span data-ttu-id="838d2-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="838d2-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="838d2-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="838d2-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="838d2-129">'A</span><span class="sxs-lookup"><span data-stu-id="838d2-129">Continue</span></span>
- <span data-ttu-id="838d2-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="838d2-130">Ignore</span></span>
- <span data-ttu-id="838d2-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="838d2-131">Inquire</span></span>
- <span data-ttu-id="838d2-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="838d2-132">SilentlyContinue</span></span>
- <span data-ttu-id="838d2-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="838d2-133">Stop</span></span>
- <span data-ttu-id="838d2-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="838d2-134">Suspend</span></span>

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

### <span data-ttu-id="838d2-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="838d2-135">-InformationVariable</span></span>
<span data-ttu-id="838d2-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="838d2-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="838d2-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="838d2-137">-Name</span></span>
<span data-ttu-id="838d2-138">Bu cmdlet 'in değiştirdiği ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="838d2-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="838d2-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="838d2-139">-NotScope</span></span>
<span data-ttu-id="838d2-140">İlke ataması kapsamlar değildir.</span><span class="sxs-lookup"><span data-stu-id="838d2-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d2-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="838d2-141">-Pre</span></span>
<span data-ttu-id="838d2-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="838d2-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="838d2-143">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="838d2-143">-Scope</span></span>
<span data-ttu-id="838d2-144">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="838d2-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="838d2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838d2-145">-DefaultProfile</span></span>
<span data-ttu-id="838d2-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="838d2-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="838d2-147">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="838d2-147">-Description</span></span>
<span data-ttu-id="838d2-148">İlke atamasının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="838d2-148">The description for policy assignment.</span></span>

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

### <span data-ttu-id="838d2-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="838d2-149">-Sku</span></span>
<span data-ttu-id="838d2-150">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="838d2-150">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838d2-151">CommonParameters</span></span>
<span data-ttu-id="838d2-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="838d2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838d2-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838d2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838d2-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="838d2-154">INPUTS</span></span>

## <span data-ttu-id="838d2-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="838d2-155">OUTPUTS</span></span>

### <span data-ttu-id="838d2-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="838d2-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="838d2-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="838d2-157">NOTES</span></span>

## <span data-ttu-id="838d2-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="838d2-158">RELATED LINKS</span></span>

[<span data-ttu-id="838d2-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="838d2-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="838d2-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="838d2-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="838d2-161">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="838d2-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


