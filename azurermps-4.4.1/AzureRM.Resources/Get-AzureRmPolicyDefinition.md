---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593807"
---
# <span data-ttu-id="76154-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76154-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="76154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76154-102">SYNOPSIS</span></span>
<span data-ttu-id="76154-103">İlke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="76154-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76154-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76154-104">SYNTAX</span></span>

### <span data-ttu-id="76154-105">Tüm ilke tanımları parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="76154-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="76154-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="76154-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76154-107">İlke tanımı adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="76154-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76154-108">İlke tanımı kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="76154-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="76154-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="76154-109">DESCRIPTION</span></span>
<span data-ttu-id="76154-110">**Get-AzureRmPolicyDefinition** cmdlet 'i, ad veya kimlikle tanımlanan tüm ilke tanımlarını veya belirli bir ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="76154-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="76154-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76154-111">EXAMPLES</span></span>

### <span data-ttu-id="76154-112">Örnek 1: tüm ilke tanımını alma</span><span class="sxs-lookup"><span data-stu-id="76154-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="76154-113">Bu komut, tüm ilke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="76154-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="76154-114">Örnek 2: ada göre ilke tanımı alma</span><span class="sxs-lookup"><span data-stu-id="76154-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="76154-115">Bu komut, VMPolicyDefinition adındaki ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="76154-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="76154-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76154-116">PARAMETERS</span></span>

### <span data-ttu-id="76154-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="76154-117">-ApiVersion</span></span>
<span data-ttu-id="76154-118">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="76154-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="76154-119">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="76154-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="76154-120">-ID</span><span class="sxs-lookup"><span data-stu-id="76154-120">-Id</span></span>
<span data-ttu-id="76154-121">Bu cmdlet 'in aldığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="76154-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="76154-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="76154-122">-InformationAction</span></span>
<span data-ttu-id="76154-123">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="76154-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76154-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="76154-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76154-125">'A</span><span class="sxs-lookup"><span data-stu-id="76154-125">Continue</span></span>
- <span data-ttu-id="76154-126">Manıza</span><span class="sxs-lookup"><span data-stu-id="76154-126">Ignore</span></span>
- <span data-ttu-id="76154-127">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="76154-127">Inquire</span></span>
- <span data-ttu-id="76154-128">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="76154-128">SilentlyContinue</span></span>
- <span data-ttu-id="76154-129">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="76154-129">Stop</span></span>
- <span data-ttu-id="76154-130">Biliriz</span><span class="sxs-lookup"><span data-stu-id="76154-130">Suspend</span></span>

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

### <span data-ttu-id="76154-131">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="76154-131">-InformationVariable</span></span>
<span data-ttu-id="76154-132">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="76154-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="76154-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="76154-133">-Name</span></span>
<span data-ttu-id="76154-134">Bu cmdlet 'in aldığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76154-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="76154-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="76154-135">-Pre</span></span>
<span data-ttu-id="76154-136">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="76154-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="76154-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76154-137">-DefaultProfile</span></span>
<span data-ttu-id="76154-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76154-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76154-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76154-139">CommonParameters</span></span>
<span data-ttu-id="76154-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76154-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76154-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76154-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76154-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76154-142">INPUTS</span></span>

## <span data-ttu-id="76154-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76154-143">OUTPUTS</span></span>

### <span data-ttu-id="76154-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="76154-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="76154-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76154-145">NOTES</span></span>

## <span data-ttu-id="76154-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76154-146">RELATED LINKS</span></span>

[<span data-ttu-id="76154-147">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76154-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="76154-148">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76154-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="76154-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76154-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


