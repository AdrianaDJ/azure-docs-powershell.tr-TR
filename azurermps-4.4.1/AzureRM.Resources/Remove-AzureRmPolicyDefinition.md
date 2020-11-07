---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764239"
---
# <span data-ttu-id="6528b-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6528b-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="6528b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6528b-102">SYNOPSIS</span></span>
<span data-ttu-id="6528b-103">İlke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6528b-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6528b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6528b-104">SYNTAX</span></span>

### <span data-ttu-id="6528b-105">İlke tanımı adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="6528b-105">The policy definition name parameter set.</span></span> <span data-ttu-id="6528b-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="6528b-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6528b-107">İlke tanımı kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="6528b-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6528b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6528b-108">DESCRIPTION</span></span>
<span data-ttu-id="6528b-109">**Remove-AzureRmPolicyDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6528b-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="6528b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6528b-110">EXAMPLES</span></span>

### <span data-ttu-id="6528b-111">Örnek 1: ilke tanımını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="6528b-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="6528b-112">Bu komut belirtilen ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6528b-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="6528b-113">Örnek 2: kaynak KIMLIĞIYLE ilke tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6528b-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="6528b-114">İlk komut, Get-AzureRmPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="6528b-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="6528b-115">Komut, $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6528b-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="6528b-116">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliğinin tanımladığı ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6528b-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="6528b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6528b-117">PARAMETERS</span></span>

### <span data-ttu-id="6528b-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="6528b-118">-ApiVersion</span></span>
<span data-ttu-id="6528b-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6528b-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6528b-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="6528b-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6528b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6528b-121">-Force</span></span>
<span data-ttu-id="6528b-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6528b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6528b-123">-ID</span><span class="sxs-lookup"><span data-stu-id="6528b-123">-Id</span></span>
<span data-ttu-id="6528b-124">Bu cmdlet 'in kaldırdığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6528b-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6528b-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6528b-125">-InformationAction</span></span>
<span data-ttu-id="6528b-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6528b-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6528b-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6528b-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6528b-128">'A</span><span class="sxs-lookup"><span data-stu-id="6528b-128">Continue</span></span>
- <span data-ttu-id="6528b-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="6528b-129">Ignore</span></span>
- <span data-ttu-id="6528b-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="6528b-130">Inquire</span></span>
- <span data-ttu-id="6528b-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="6528b-131">SilentlyContinue</span></span>
- <span data-ttu-id="6528b-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="6528b-132">Stop</span></span>
- <span data-ttu-id="6528b-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="6528b-133">Suspend</span></span>

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

### <span data-ttu-id="6528b-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="6528b-134">-InformationVariable</span></span>
<span data-ttu-id="6528b-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="6528b-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6528b-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="6528b-136">-Name</span></span>
<span data-ttu-id="6528b-137">Bu cmdlet 'in kaldırdığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6528b-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6528b-138">-Pre-</span><span class="sxs-lookup"><span data-stu-id="6528b-138">-Pre</span></span>
<span data-ttu-id="6528b-139">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6528b-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6528b-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="6528b-140">-Confirm</span></span>
<span data-ttu-id="6528b-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6528b-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6528b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6528b-142">-WhatIf</span></span>
<span data-ttu-id="6528b-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6528b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6528b-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6528b-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6528b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6528b-145">-DefaultProfile</span></span>
<span data-ttu-id="6528b-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6528b-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6528b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6528b-147">CommonParameters</span></span>
<span data-ttu-id="6528b-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6528b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6528b-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6528b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6528b-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6528b-150">INPUTS</span></span>

## <span data-ttu-id="6528b-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6528b-151">OUTPUTS</span></span>

### <span data-ttu-id="6528b-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6528b-152">System.Boolean</span></span>

## <span data-ttu-id="6528b-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6528b-153">NOTES</span></span>

## <span data-ttu-id="6528b-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6528b-154">RELATED LINKS</span></span>

[<span data-ttu-id="6528b-155">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6528b-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6528b-156">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6528b-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6528b-157">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6528b-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


