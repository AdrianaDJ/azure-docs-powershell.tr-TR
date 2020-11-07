---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: 8cd1ee1d8f32bd203e9fb2d8ac5d75c2d6b2938d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936345"
---
# <span data-ttu-id="cb7ed-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cb7ed-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="cb7ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7ed-103">İlke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-103">Removes a policy definition.</span></span>

## <span data-ttu-id="cb7ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb7ed-104">SYNTAX</span></span>

### <span data-ttu-id="cb7ed-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb7ed-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb7ed-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb7ed-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb7ed-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cb7ed-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb7ed-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="cb7ed-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb7ed-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb7ed-109">DESCRIPTION</span></span>
<span data-ttu-id="cb7ed-110">**Remove-AzPolicyDefinition** cmdlet 'i bir ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="cb7ed-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb7ed-111">EXAMPLES</span></span>

### <span data-ttu-id="cb7ed-112">Örnek 1: ilke tanımını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="cb7ed-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="cb7ed-113">Bu komut belirtilen ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="cb7ed-114">Örnek 2: kaynak KIMLIĞIYLE ilke tanımını kaldırma</span><span class="sxs-lookup"><span data-stu-id="cb7ed-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="cb7ed-115">İlk komut, Get-AzPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="cb7ed-116">Komut, $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="cb7ed-117">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliğinin tanımladığı ilke tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="cb7ed-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb7ed-118">PARAMETERS</span></span>

### <span data-ttu-id="cb7ed-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="cb7ed-119">-ApiVersion</span></span>
<span data-ttu-id="cb7ed-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cb7ed-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cb7ed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7ed-122">-DefaultProfile</span></span>
<span data-ttu-id="cb7ed-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cb7ed-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb7ed-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cb7ed-124">-Force</span></span>
<span data-ttu-id="cb7ed-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb7ed-126">-ID</span><span class="sxs-lookup"><span data-stu-id="cb7ed-126">-Id</span></span>
<span data-ttu-id="cb7ed-127">Bu cmdlet 'in kaldırdığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb7ed-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cb7ed-128">-InformationAction</span></span>
<span data-ttu-id="cb7ed-129">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="cb7ed-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cb7ed-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb7ed-131">'A</span><span class="sxs-lookup"><span data-stu-id="cb7ed-131">Continue</span></span>
- <span data-ttu-id="cb7ed-132">Manıza</span><span class="sxs-lookup"><span data-stu-id="cb7ed-132">Ignore</span></span>
- <span data-ttu-id="cb7ed-133">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="cb7ed-133">Inquire</span></span>
- <span data-ttu-id="cb7ed-134">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="cb7ed-134">SilentlyContinue</span></span>
- <span data-ttu-id="cb7ed-135">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="cb7ed-135">Stop</span></span>
- <span data-ttu-id="cb7ed-136">Biliriz</span><span class="sxs-lookup"><span data-stu-id="cb7ed-136">Suspend</span></span>

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

### <span data-ttu-id="cb7ed-137">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="cb7ed-137">-InformationVariable</span></span>
<span data-ttu-id="cb7ed-138">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cb7ed-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="cb7ed-139">-ManagementGroupName</span></span>
<span data-ttu-id="cb7ed-140">Silinecek ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-140">The name of the management group of the policy definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb7ed-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb7ed-141">-Name</span></span>
<span data-ttu-id="cb7ed-142">Bu cmdlet 'in kaldırdığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb7ed-143">-Pre-</span><span class="sxs-lookup"><span data-stu-id="cb7ed-143">-Pre</span></span>
<span data-ttu-id="cb7ed-144">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cb7ed-145">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cb7ed-145">-SubscriptionId</span></span>
<span data-ttu-id="cb7ed-146">Silinecek ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-146">The subscription ID of the policy definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb7ed-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb7ed-147">-Confirm</span></span>
<span data-ttu-id="cb7ed-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb7ed-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb7ed-149">-WhatIf</span></span>
<span data-ttu-id="cb7ed-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb7ed-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb7ed-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7ed-152">CommonParameters</span></span>
<span data-ttu-id="cb7ed-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb7ed-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7ed-154">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb7ed-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7ed-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb7ed-155">INPUTS</span></span>

## <span data-ttu-id="cb7ed-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb7ed-156">OUTPUTS</span></span>

## <span data-ttu-id="cb7ed-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb7ed-157">NOTES</span></span>

## <span data-ttu-id="cb7ed-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb7ed-158">RELATED LINKS</span></span>

[<span data-ttu-id="cb7ed-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cb7ed-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="cb7ed-160">Yeni-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="cb7ed-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="cb7ed-161">Set-Azilketanımı</span><span class="sxs-lookup"><span data-stu-id="cb7ed-161">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


