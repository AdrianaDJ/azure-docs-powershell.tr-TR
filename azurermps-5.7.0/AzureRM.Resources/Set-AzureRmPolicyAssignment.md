---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593429"
---
# <span data-ttu-id="36f38-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="36f38-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="36f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f38-102">SYNOPSIS</span></span>
<span data-ttu-id="36f38-103">Bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="36f38-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36f38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36f38-104">SYNTAX</span></span>

### <span data-ttu-id="36f38-105">SetByPolicyAssignmentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36f38-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="36f38-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="36f38-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="36f38-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="36f38-107">DESCRIPTION</span></span>
<span data-ttu-id="36f38-108">**Set-AzureRmPolicyAssignment** cmdlet 'i bir ilke atamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="36f38-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="36f38-109">KIMLIĞE göre veya ad ve kapsamla bir ödev belirtin.</span><span class="sxs-lookup"><span data-stu-id="36f38-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="36f38-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36f38-110">EXAMPLES</span></span>

### <span data-ttu-id="36f38-111">Örnek 1: görünen adı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="36f38-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="36f38-112">İlk komut, Get-AzureRMResourceGroup cmdlet 'ini kullanarak ResourceGroup11 adlı bir kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="36f38-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="36f38-113">Komut bu nesneyi $ResourceGroup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="36f38-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="36f38-114">İkinci komut, Get-AzureRmPolicyAssignment cmdlet 'ini kullanarak PolicyAssignment adındaki ilke atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="36f38-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="36f38-115">Komut bu nesneyi $PolicyAssignment değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="36f38-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="36f38-116">Son komutu, $PolicyAssignment 'un **RESOURCEID** özelliğiyle tanımlanan ilke atamasında görünen adı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36f38-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="36f38-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36f38-117">PARAMETERS</span></span>

### <span data-ttu-id="36f38-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="36f38-118">-ApiVersion</span></span>
<span data-ttu-id="36f38-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f38-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="36f38-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="36f38-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="36f38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f38-121">-DefaultProfile</span></span>
<span data-ttu-id="36f38-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="36f38-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36f38-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="36f38-123">-Description</span></span>
<span data-ttu-id="36f38-124">İlke atamasının açıklaması</span><span class="sxs-lookup"><span data-stu-id="36f38-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f38-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="36f38-125">-DisplayName</span></span>
<span data-ttu-id="36f38-126">İlke ataması için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f38-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f38-127">-ID</span><span class="sxs-lookup"><span data-stu-id="36f38-127">-Id</span></span>
<span data-ttu-id="36f38-128">Bu cmdlet 'in değiştirdiği ilke atamasının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f38-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f38-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="36f38-129">-InformationAction</span></span>
<span data-ttu-id="36f38-130">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f38-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="36f38-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="36f38-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36f38-132">'A</span><span class="sxs-lookup"><span data-stu-id="36f38-132">Continue</span></span>
- <span data-ttu-id="36f38-133">Manıza</span><span class="sxs-lookup"><span data-stu-id="36f38-133">Ignore</span></span>
- <span data-ttu-id="36f38-134">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="36f38-134">Inquire</span></span>
- <span data-ttu-id="36f38-135">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="36f38-135">SilentlyContinue</span></span>
- <span data-ttu-id="36f38-136">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="36f38-136">Stop</span></span>
- <span data-ttu-id="36f38-137">Biliriz</span><span class="sxs-lookup"><span data-stu-id="36f38-137">Suspend</span></span>

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

### <span data-ttu-id="36f38-138">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="36f38-138">-InformationVariable</span></span>
<span data-ttu-id="36f38-139">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f38-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="36f38-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="36f38-140">-Name</span></span>
<span data-ttu-id="36f38-141">Bu cmdlet 'in değiştirdiği ilke atamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f38-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f38-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="36f38-142">-NotScope</span></span>
<span data-ttu-id="36f38-143">İlke ataması kapsamlar değildir.</span><span class="sxs-lookup"><span data-stu-id="36f38-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f38-144">-Pre-</span><span class="sxs-lookup"><span data-stu-id="36f38-144">-Pre</span></span>
<span data-ttu-id="36f38-145">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="36f38-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="36f38-146">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="36f38-146">-Scope</span></span>
<span data-ttu-id="36f38-147">İlkenin uygulandığı kapsamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f38-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f38-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="36f38-148">-Sku</span></span>
<span data-ttu-id="36f38-149">SKU özelliklerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="36f38-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f38-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f38-150">CommonParameters</span></span>
<span data-ttu-id="36f38-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36f38-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f38-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f38-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f38-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36f38-153">INPUTS</span></span>

### <span data-ttu-id="36f38-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="36f38-154">None</span></span>
<span data-ttu-id="36f38-155">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="36f38-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36f38-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36f38-156">OUTPUTS</span></span>

### <span data-ttu-id="36f38-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="36f38-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="36f38-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36f38-158">NOTES</span></span>

## <span data-ttu-id="36f38-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36f38-159">RELATED LINKS</span></span>

[<span data-ttu-id="36f38-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="36f38-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="36f38-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="36f38-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="36f38-162">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="36f38-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


