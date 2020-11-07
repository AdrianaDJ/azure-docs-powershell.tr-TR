---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: aa6687efb331cbb702ea36c53cc02cd77cefd45d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939042"
---
# <span data-ttu-id="cd6c1-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cd6c1-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="cd6c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6c1-103">İlke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd6c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd6c1-104">SYNTAX</span></span>

### <span data-ttu-id="cd6c1-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd6c1-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd6c1-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd6c1-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd6c1-107">Subscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cd6c1-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd6c1-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="cd6c1-108">IdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cd6c1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd6c1-109">DESCRIPTION</span></span>
<span data-ttu-id="cd6c1-110">**Set-AzureRmPolicyDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-110">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="cd6c1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd6c1-111">EXAMPLES</span></span>

### <span data-ttu-id="cd6c1-112">Örnek 1: ilke tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cd6c1-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="cd6c1-113">İlk komut, Get-AzureRmPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="cd6c1-114">Komut bu nesneyi $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="cd6c1-115">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliği tarafından tanımlanan ilke tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="cd6c1-116">Örnek 2: ilke tanımının modunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cd6c1-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="cd6c1-117">Bu komut, VMPolicyDefinition adındaki ilke tanımını, Mode özelliğini ' All ' olarak ayarlamak için Set-AzureRmPolicyDefinition cmdlet 'ini kullanarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzureRmPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="cd6c1-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd6c1-118">PARAMETERS</span></span>

### <span data-ttu-id="cd6c1-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="cd6c1-119">-ApiVersion</span></span>
<span data-ttu-id="cd6c1-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cd6c1-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cd6c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6c1-122">-DefaultProfile</span></span>
<span data-ttu-id="cd6c1-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cd6c1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd6c1-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="cd6c1-124">-Description</span></span>
<span data-ttu-id="cd6c1-125">İlke tanımı için yeni bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="cd6c1-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd6c1-126">-DisplayName</span></span>
<span data-ttu-id="cd6c1-127">İlke tanımı için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="cd6c1-128">-ID</span><span class="sxs-lookup"><span data-stu-id="cd6c1-128">-Id</span></span>
<span data-ttu-id="cd6c1-129">Bu cmdlet 'in değiştirdiği ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cd6c1-130">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cd6c1-130">-InformationAction</span></span>
<span data-ttu-id="cd6c1-131">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="cd6c1-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cd6c1-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd6c1-133">'A</span><span class="sxs-lookup"><span data-stu-id="cd6c1-133">Continue</span></span>
- <span data-ttu-id="cd6c1-134">Manıza</span><span class="sxs-lookup"><span data-stu-id="cd6c1-134">Ignore</span></span>
- <span data-ttu-id="cd6c1-135">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="cd6c1-135">Inquire</span></span>
- <span data-ttu-id="cd6c1-136">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="cd6c1-136">SilentlyContinue</span></span>
- <span data-ttu-id="cd6c1-137">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="cd6c1-137">Stop</span></span>
- <span data-ttu-id="cd6c1-138">Biliriz</span><span class="sxs-lookup"><span data-stu-id="cd6c1-138">Suspend</span></span>

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

### <span data-ttu-id="cd6c1-139">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="cd6c1-139">-InformationVariable</span></span>
<span data-ttu-id="cd6c1-140">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cd6c1-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6c1-141">-ManagementGroupName</span></span>
<span data-ttu-id="cd6c1-142">Güncelleştirilecek ilke tanımının yönetim grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="cd6c1-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cd6c1-143">-Metadata</span></span>
<span data-ttu-id="cd6c1-144">İlke tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-144">The metadata for policy definition.</span></span> <span data-ttu-id="cd6c1-145">Bu, meta veri veya meta veri içeren bir dosya adının yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="cd6c1-146">-Mod</span><span class="sxs-lookup"><span data-stu-id="cd6c1-146">-Mode</span></span>
<span data-ttu-id="cd6c1-147">Yeni ilke tanımının modu.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-147">The mode of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6c1-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd6c1-148">-Name</span></span>
<span data-ttu-id="cd6c1-149">Bu cmdlet 'in değiştirdiği ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6c1-150">-Parametre</span><span class="sxs-lookup"><span data-stu-id="cd6c1-150">-Parameter</span></span>
<span data-ttu-id="cd6c1-151">İlke tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="cd6c1-152">Bu, parametre bildirimini içeren bir dosya adı veya URI veya dize olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="cd6c1-153">-İlke</span><span class="sxs-lookup"><span data-stu-id="cd6c1-153">-Policy</span></span>
<span data-ttu-id="cd6c1-154">İlke tanımı için yeni ilke kuralı belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="cd6c1-155">Bir. json dosyasının veya JavaScript nesne gösterimi (JSON) biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="cd6c1-156">-Pre-</span><span class="sxs-lookup"><span data-stu-id="cd6c1-156">-Pre</span></span>
<span data-ttu-id="cd6c1-157">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cd6c1-158">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cd6c1-158">-SubscriptionId</span></span>
<span data-ttu-id="cd6c1-159">Güncelleştirilecek ilke tanımının abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="cd6c1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6c1-160">CommonParameters</span></span>
<span data-ttu-id="cd6c1-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd6c1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6c1-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd6c1-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6c1-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd6c1-163">INPUTS</span></span>

## <span data-ttu-id="cd6c1-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd6c1-164">OUTPUTS</span></span>

## <span data-ttu-id="cd6c1-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd6c1-165">NOTES</span></span>

## <span data-ttu-id="cd6c1-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd6c1-166">RELATED LINKS</span></span>

[<span data-ttu-id="cd6c1-167">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cd6c1-167">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="cd6c1-168">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cd6c1-168">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="cd6c1-169">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cd6c1-169">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


