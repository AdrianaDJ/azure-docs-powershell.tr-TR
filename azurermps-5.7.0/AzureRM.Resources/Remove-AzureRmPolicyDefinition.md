---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762142"
---
# <span data-ttu-id="870af-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="870af-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="870af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="870af-102">SYNOPSIS</span></span>
<span data-ttu-id="870af-103">İlke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="870af-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="870af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="870af-104">SYNTAX</span></span>

### <span data-ttu-id="870af-105">RemoveByPolicyDefinitionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="870af-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="870af-106">Removebypolicydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="870af-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="870af-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="870af-107">DESCRIPTION</span></span>
<span data-ttu-id="870af-108">**Remove-AzureRmPolicyDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="870af-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="870af-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="870af-109">EXAMPLES</span></span>

### <span data-ttu-id="870af-110">Örnek 1: ilke tanımını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="870af-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="870af-111">Bu komut belirtilen ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="870af-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="870af-112">Örnek 2: kaynak KIMLIĞIYLE ilke tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="870af-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="870af-113">İlk komut, Get-AzureRmPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="870af-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="870af-114">Komut, $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="870af-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="870af-115">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliğinin tanımladığı ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="870af-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="870af-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="870af-116">PARAMETERS</span></span>

### <span data-ttu-id="870af-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="870af-117">-ApiVersion</span></span>
<span data-ttu-id="870af-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="870af-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="870af-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="870af-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="870af-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870af-120">-DefaultProfile</span></span>
<span data-ttu-id="870af-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="870af-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="870af-122">-Force</span><span class="sxs-lookup"><span data-stu-id="870af-122">-Force</span></span>
<span data-ttu-id="870af-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="870af-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="870af-124">-ID</span><span class="sxs-lookup"><span data-stu-id="870af-124">-Id</span></span>
<span data-ttu-id="870af-125">Bu cmdlet 'in kaldırdığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="870af-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870af-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="870af-126">-InformationAction</span></span>
<span data-ttu-id="870af-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="870af-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="870af-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="870af-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="870af-129">'A</span><span class="sxs-lookup"><span data-stu-id="870af-129">Continue</span></span>
- <span data-ttu-id="870af-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="870af-130">Ignore</span></span>
- <span data-ttu-id="870af-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="870af-131">Inquire</span></span>
- <span data-ttu-id="870af-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="870af-132">SilentlyContinue</span></span>
- <span data-ttu-id="870af-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="870af-133">Stop</span></span>
- <span data-ttu-id="870af-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="870af-134">Suspend</span></span>

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

### <span data-ttu-id="870af-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="870af-135">-InformationVariable</span></span>
<span data-ttu-id="870af-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="870af-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="870af-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="870af-137">-Name</span></span>
<span data-ttu-id="870af-138">Bu cmdlet 'in kaldırdığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="870af-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870af-139">-Pre-</span><span class="sxs-lookup"><span data-stu-id="870af-139">-Pre</span></span>
<span data-ttu-id="870af-140">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="870af-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="870af-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="870af-141">-Confirm</span></span>
<span data-ttu-id="870af-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="870af-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870af-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="870af-143">-WhatIf</span></span>
<span data-ttu-id="870af-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="870af-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="870af-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="870af-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="870af-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870af-146">CommonParameters</span></span>
<span data-ttu-id="870af-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="870af-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870af-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="870af-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870af-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="870af-149">INPUTS</span></span>

### <span data-ttu-id="870af-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="870af-150">None</span></span>
<span data-ttu-id="870af-151">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="870af-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="870af-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="870af-152">OUTPUTS</span></span>

### <span data-ttu-id="870af-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="870af-153">System.Boolean</span></span>

## <span data-ttu-id="870af-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="870af-154">NOTES</span></span>

## <span data-ttu-id="870af-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="870af-155">RELATED LINKS</span></span>

[<span data-ttu-id="870af-156">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="870af-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="870af-157">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="870af-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="870af-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="870af-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


