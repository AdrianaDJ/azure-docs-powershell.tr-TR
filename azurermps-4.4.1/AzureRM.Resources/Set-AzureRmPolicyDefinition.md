---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764236"
---
# <span data-ttu-id="35ac0-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="35ac0-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="35ac0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="35ac0-103">İlke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35ac0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35ac0-104">SYNTAX</span></span>

### <span data-ttu-id="35ac0-105">İlke tanımı adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="35ac0-105">The policy definition name parameter set.</span></span> <span data-ttu-id="35ac0-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="35ac0-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="35ac0-107">İlke tanımı kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="35ac0-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="35ac0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="35ac0-108">DESCRIPTION</span></span>
<span data-ttu-id="35ac0-109">**Set-AzureRmPolicyDefinition** cmdlet 'i bir ilke tanımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="35ac0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35ac0-110">EXAMPLES</span></span>

### <span data-ttu-id="35ac0-111">Örnek 1: ilke tanımının açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="35ac0-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="35ac0-112">İlk komut, Get-AzureRmPolicyDefinition cmdlet 'ini kullanarak VMPolicyDefinition adlı bir ilke tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="35ac0-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="35ac0-113">Komut bu nesneyi $PolicyDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="35ac0-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="35ac0-114">İkinci komut $PolicyDefinition 'in **RESOURCEID** özelliği tarafından tanımlanan ilke tanımının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="35ac0-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="35ac0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35ac0-115">PARAMETERS</span></span>

### <span data-ttu-id="35ac0-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="35ac0-116">-ApiVersion</span></span>
<span data-ttu-id="35ac0-117">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="35ac0-118">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="35ac0-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="35ac0-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="35ac0-119">-Description</span></span>
<span data-ttu-id="35ac0-120">İlke tanımı için yeni bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-120">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="35ac0-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="35ac0-121">-DisplayName</span></span>
<span data-ttu-id="35ac0-122">İlke tanımı için yeni bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-122">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="35ac0-123">-ID</span><span class="sxs-lookup"><span data-stu-id="35ac0-123">-Id</span></span>
<span data-ttu-id="35ac0-124">Bu cmdlet 'in değiştirdiği ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35ac0-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="35ac0-125">-InformationAction</span></span>
<span data-ttu-id="35ac0-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="35ac0-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="35ac0-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35ac0-128">'A</span><span class="sxs-lookup"><span data-stu-id="35ac0-128">Continue</span></span>
- <span data-ttu-id="35ac0-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="35ac0-129">Ignore</span></span>
- <span data-ttu-id="35ac0-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="35ac0-130">Inquire</span></span>
- <span data-ttu-id="35ac0-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="35ac0-131">SilentlyContinue</span></span>
- <span data-ttu-id="35ac0-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="35ac0-132">Stop</span></span>
- <span data-ttu-id="35ac0-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="35ac0-133">Suspend</span></span>

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

### <span data-ttu-id="35ac0-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="35ac0-134">-InformationVariable</span></span>
<span data-ttu-id="35ac0-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="35ac0-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="35ac0-136">-Name</span></span>
<span data-ttu-id="35ac0-137">Bu cmdlet 'in değiştirdiği ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35ac0-138">-İlke</span><span class="sxs-lookup"><span data-stu-id="35ac0-138">-Policy</span></span>
<span data-ttu-id="35ac0-139">İlke tanımı için yeni ilke kuralı belirtir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="35ac0-140">Bir. json dosyasının veya JavaScript nesne gösterimi (JSON) biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="35ac0-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="35ac0-141">-Pre-</span><span class="sxs-lookup"><span data-stu-id="35ac0-141">-Pre</span></span>
<span data-ttu-id="35ac0-142">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="35ac0-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ac0-143">-DefaultProfile</span></span>
<span data-ttu-id="35ac0-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35ac0-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35ac0-145">-Metadata</span><span class="sxs-lookup"><span data-stu-id="35ac0-145">-Metadata</span></span>
<span data-ttu-id="35ac0-146">İlke tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="35ac0-146">The metadata for policy definition.</span></span> <span data-ttu-id="35ac0-147">Bu, meta veri veya meta veri içeren bir dosya adının yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="35ac0-148">-Parametre</span><span class="sxs-lookup"><span data-stu-id="35ac0-148">-Parameter</span></span>
<span data-ttu-id="35ac0-149">İlke tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="35ac0-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="35ac0-150">Bu, parametre bildirimini içeren bir dosya adı veya URI veya dize olarak parametre bildirimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="35ac0-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="35ac0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ac0-151">CommonParameters</span></span>
<span data-ttu-id="35ac0-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35ac0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ac0-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ac0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ac0-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35ac0-154">INPUTS</span></span>

## <span data-ttu-id="35ac0-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35ac0-155">OUTPUTS</span></span>

### <span data-ttu-id="35ac0-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="35ac0-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="35ac0-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35ac0-157">NOTES</span></span>

## <span data-ttu-id="35ac0-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35ac0-158">RELATED LINKS</span></span>

[<span data-ttu-id="35ac0-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="35ac0-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="35ac0-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="35ac0-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="35ac0-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="35ac0-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


