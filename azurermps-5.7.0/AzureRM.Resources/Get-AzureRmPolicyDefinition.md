---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592911"
---
# <span data-ttu-id="9e0aa-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9e0aa-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="9e0aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0aa-103">İlke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e0aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e0aa-104">SYNTAX</span></span>

### <span data-ttu-id="9e0aa-105">GetAllPolicyDefinitions (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e0aa-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9e0aa-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="9e0aa-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9e0aa-107">Getbypolicydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="9e0aa-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9e0aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e0aa-108">DESCRIPTION</span></span>
<span data-ttu-id="9e0aa-109">**Get-AzureRmPolicyDefinition** cmdlet 'i, ad veya kimlikle tanımlanan tüm ilke tanımlarını veya belirli bir ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="9e0aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e0aa-110">EXAMPLES</span></span>

### <span data-ttu-id="9e0aa-111">Örnek 1: tüm ilke tanımını alma</span><span class="sxs-lookup"><span data-stu-id="9e0aa-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="9e0aa-112">Bu komut, tüm ilke tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="9e0aa-113">Örnek 2: ada göre ilke tanımı alma</span><span class="sxs-lookup"><span data-stu-id="9e0aa-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="9e0aa-114">Bu komut, VMPolicyDefinition adındaki ilke tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="9e0aa-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e0aa-115">PARAMETERS</span></span>

### <span data-ttu-id="9e0aa-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="9e0aa-116">-ApiVersion</span></span>
<span data-ttu-id="9e0aa-117">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9e0aa-118">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9e0aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0aa-119">-DefaultProfile</span></span>
<span data-ttu-id="9e0aa-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9e0aa-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e0aa-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9e0aa-121">-Id</span></span>
<span data-ttu-id="9e0aa-122">Bu cmdlet 'in aldığı ilke tanımının tam nitelikli kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0aa-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9e0aa-123">-InformationAction</span></span>
<span data-ttu-id="9e0aa-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9e0aa-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9e0aa-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e0aa-126">'A</span><span class="sxs-lookup"><span data-stu-id="9e0aa-126">Continue</span></span>
- <span data-ttu-id="9e0aa-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="9e0aa-127">Ignore</span></span>
- <span data-ttu-id="9e0aa-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="9e0aa-128">Inquire</span></span>
- <span data-ttu-id="9e0aa-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="9e0aa-129">SilentlyContinue</span></span>
- <span data-ttu-id="9e0aa-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="9e0aa-130">Stop</span></span>
- <span data-ttu-id="9e0aa-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="9e0aa-131">Suspend</span></span>

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

### <span data-ttu-id="9e0aa-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="9e0aa-132">-InformationVariable</span></span>
<span data-ttu-id="9e0aa-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9e0aa-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e0aa-134">-Name</span></span>
<span data-ttu-id="9e0aa-135">Bu cmdlet 'in aldığı ilke tanımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0aa-136">-Pre-</span><span class="sxs-lookup"><span data-stu-id="9e0aa-136">-Pre</span></span>
<span data-ttu-id="9e0aa-137">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9e0aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0aa-138">CommonParameters</span></span>
<span data-ttu-id="9e0aa-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0aa-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e0aa-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0aa-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e0aa-141">INPUTS</span></span>

### <span data-ttu-id="9e0aa-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9e0aa-142">None</span></span>
<span data-ttu-id="9e0aa-143">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9e0aa-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e0aa-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e0aa-144">OUTPUTS</span></span>

### <span data-ttu-id="9e0aa-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9e0aa-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9e0aa-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e0aa-146">NOTES</span></span>

## <span data-ttu-id="9e0aa-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e0aa-147">RELATED LINKS</span></span>

[<span data-ttu-id="9e0aa-148">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9e0aa-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="9e0aa-149">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9e0aa-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="9e0aa-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9e0aa-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


