---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: e39d60863b9409a6d52f2f92dc312e98b8e50cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588799"
---
# <span data-ttu-id="1dd3d-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1dd3d-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="1dd3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd3d-103">İlke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dd3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dd3d-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1dd3d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dd3d-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd3d-106">**New-AzureRmPolicyDefinition** cmdlet 'ı JavaScript nesne GÖSTERIMI (JSON) biçiminde ilke kuralı içeren bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="1dd3d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dd3d-107">EXAMPLES</span></span>

### <span data-ttu-id="1dd3d-108">Örnek 1: ilke dosyası kullanarak ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1dd3d-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="1dd3d-109">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke kuralını içeren VMPolicyDefinition adlı bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="1dd3d-110">Örnek 2: satır içi ilke tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1dd3d-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="1dd3d-111">Bu komut VMPolicyDefinition adlı bir ilke tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="1dd3d-112">Komut ilkeyi geçerli JSON biçiminde bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="1dd3d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dd3d-113">PARAMETERS</span></span>

### <span data-ttu-id="1dd3d-114">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="1dd3d-114">-ApiVersion</span></span>
<span data-ttu-id="1dd3d-115">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1dd3d-116">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1dd3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd3d-117">-DefaultProfile</span></span>
<span data-ttu-id="1dd3d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1dd3d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dd3d-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="1dd3d-119">-Description</span></span>
<span data-ttu-id="1dd3d-120">İlke tanımının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-120">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="1dd3d-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1dd3d-121">-DisplayName</span></span>
<span data-ttu-id="1dd3d-122">İlke tanımı için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-122">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="1dd3d-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1dd3d-123">-InformationAction</span></span>
<span data-ttu-id="1dd3d-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1dd3d-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1dd3d-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1dd3d-126">'A</span><span class="sxs-lookup"><span data-stu-id="1dd3d-126">Continue</span></span>
- <span data-ttu-id="1dd3d-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="1dd3d-127">Ignore</span></span>
- <span data-ttu-id="1dd3d-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="1dd3d-128">Inquire</span></span>
- <span data-ttu-id="1dd3d-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="1dd3d-129">SilentlyContinue</span></span>
- <span data-ttu-id="1dd3d-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="1dd3d-130">Stop</span></span>
- <span data-ttu-id="1dd3d-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="1dd3d-131">Suspend</span></span>

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

### <span data-ttu-id="1dd3d-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="1dd3d-132">-InformationVariable</span></span>
<span data-ttu-id="1dd3d-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1dd3d-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1dd3d-134">-Metadata</span></span>
<span data-ttu-id="1dd3d-135">İlke tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-135">The metadata for policy definition.</span></span> <span data-ttu-id="1dd3d-136">Bu, meta veri içeren bir dosya adının yolu veya dize olarak meta veri olabilir</span><span class="sxs-lookup"><span data-stu-id="1dd3d-136">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="1dd3d-137">-Mod</span><span class="sxs-lookup"><span data-stu-id="1dd3d-137">-Mode</span></span>
<span data-ttu-id="1dd3d-138">İlke tanımının modu</span><span class="sxs-lookup"><span data-stu-id="1dd3d-138">The mode of the policy definition</span></span>

```yaml
Type: PolicyDefinitionMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd3d-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="1dd3d-139">-Name</span></span>
<span data-ttu-id="1dd3d-140">İlke tanımı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-140">Specifies a name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd3d-141">-Parametre</span><span class="sxs-lookup"><span data-stu-id="1dd3d-141">-Parameter</span></span>
<span data-ttu-id="1dd3d-142">İlke tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="1dd3d-143">Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-143">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="1dd3d-144">-İlke</span><span class="sxs-lookup"><span data-stu-id="1dd3d-144">-Policy</span></span>
<span data-ttu-id="1dd3d-145">İlke tanımı için bir ilke kuralı belirtir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-145">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="1dd3d-146">. Json dosyasının veya JSON biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-146">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd3d-147">-Pre-</span><span class="sxs-lookup"><span data-stu-id="1dd3d-147">-Pre</span></span>
<span data-ttu-id="1dd3d-148">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1dd3d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd3d-149">CommonParameters</span></span>
<span data-ttu-id="1dd3d-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd3d-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd3d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd3d-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dd3d-152">INPUTS</span></span>

### <span data-ttu-id="1dd3d-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1dd3d-153">None</span></span>
<span data-ttu-id="1dd3d-154">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1dd3d-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1dd3d-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dd3d-155">OUTPUTS</span></span>

### <span data-ttu-id="1dd3d-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1dd3d-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1dd3d-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dd3d-157">NOTES</span></span>

## <span data-ttu-id="1dd3d-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dd3d-158">RELATED LINKS</span></span>

[<span data-ttu-id="1dd3d-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1dd3d-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="1dd3d-160">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1dd3d-160">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="1dd3d-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1dd3d-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


