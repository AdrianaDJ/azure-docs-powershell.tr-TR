---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108340"
---
# <span data-ttu-id="50f45-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="50f45-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="50f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f45-102">SYNOPSIS</span></span>
<span data-ttu-id="50f45-103">Veri paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50f45-103">Removes a data share.</span></span>

## <span data-ttu-id="50f45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50f45-104">SYNTAX</span></span>

### <span data-ttu-id="50f45-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50f45-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f45-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="50f45-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f45-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f45-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50f45-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="50f45-108">DESCRIPTION</span></span>
<span data-ttu-id="50f45-109">**Remove-AzDataShare** cmdlet 'i veri paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50f45-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="50f45-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50f45-110">EXAMPLES</span></span>

### <span data-ttu-id="50f45-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="50f45-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="50f45-112">Bu komut, Azure veri paylaşımı hesap WikiAds adındaki AdsShare adlı veri paylaşımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50f45-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="50f45-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50f45-113">PARAMETERS</span></span>

### <span data-ttu-id="50f45-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="50f45-114">-AccountName</span></span>
<span data-ttu-id="50f45-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="50f45-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f45-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="50f45-116">-AsJob</span></span>
<span data-ttu-id="50f45-117">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="50f45-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="50f45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f45-118">-DefaultProfile</span></span>
<span data-ttu-id="50f45-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50f45-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f45-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50f45-120">-InputObject</span></span>
<span data-ttu-id="50f45-121">Azure veri paylaşımı nesnesi ' ' ' YAML türü: PSDataShare parametre kümeleri: ByObjectParameterSet diğer adları:</span><span class="sxs-lookup"><span data-stu-id="50f45-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="50f45-122">Gerekli: doğru konum: adlandırılmış varsayılan değer: None kabul etme girişi: doğru (ByValue) joker karakterleri kabul et: false</span><span class="sxs-lookup"><span data-stu-id="50f45-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50f45-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="50f45-123">-Name</span></span>
<span data-ttu-id="50f45-124">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="50f45-124">Azure data share name</span></span>

<span data-ttu-id="50f45-125">YAML türü: dize parametre kümeleri: ByFieldsParameterSet diğer adları:</span><span class="sxs-lookup"><span data-stu-id="50f45-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="50f45-126">Gerekli: doğru konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false</span><span class="sxs-lookup"><span data-stu-id="50f45-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f45-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="50f45-127">-PassThru</span></span>
<span data-ttu-id="50f45-128">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="50f45-128">Return object (if specified).</span></span>

<span data-ttu-id="50f45-129">YAML türü: SwitchParameter parametre kümeleri: (tümü) diğer adlar:</span><span class="sxs-lookup"><span data-stu-id="50f45-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="50f45-130">Gerekli: yanlış konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false</span><span class="sxs-lookup"><span data-stu-id="50f45-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="50f45-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f45-131">-ResourceGroupName</span></span>
<span data-ttu-id="50f45-132">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="50f45-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="50f45-133">YAML türü: dize parametre kümeleri: ByFieldsParameterSet diğer adları:</span><span class="sxs-lookup"><span data-stu-id="50f45-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="50f45-134">Gerekli: doğru konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false</span><span class="sxs-lookup"><span data-stu-id="50f45-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f45-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="50f45-135">-ResourceId</span></span>
<span data-ttu-id="50f45-136">Azure veri paylaşımı 'nın kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="50f45-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="50f45-137">YAML türü: dize parametre kümeleri: Byresourceıdparameterset diğer adları:</span><span class="sxs-lookup"><span data-stu-id="50f45-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="50f45-138">Gerekli: doğru konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: true (ByPropertyName) joker karakter kabul et: false</span><span class="sxs-lookup"><span data-stu-id="50f45-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50f45-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="50f45-139">-Confirm</span></span>
<span data-ttu-id="50f45-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50f45-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="50f45-141">YAML türü: SwitchParameter parametre kümeleri: (tümü) diğer adlar: CF</span><span class="sxs-lookup"><span data-stu-id="50f45-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="50f45-142">Gerekli: yanlış konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false</span><span class="sxs-lookup"><span data-stu-id="50f45-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f45-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50f45-143">-WhatIf</span></span>
<span data-ttu-id="50f45-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50f45-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50f45-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50f45-145">The cmdlet is not run.</span></span>

<span data-ttu-id="50f45-146">YAML türü: SwitchParameter parametre kümeleri: (tümü) diğer adlar: WI</span><span class="sxs-lookup"><span data-stu-id="50f45-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="50f45-147">Gerekli: yanlış konum: adlandırılmış varsayılan değer: None Accept Pipeline Input: false joker karakterlerini kabul et: false</span><span class="sxs-lookup"><span data-stu-id="50f45-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="50f45-148">YAML türü: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı parametre kümeleri: ByObjectParameterSet diğer adları:</span><span class="sxs-lookup"><span data-stu-id="50f45-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="50f45-149">Gerekli: doğru konum: adlandırılmış varsayılan değer: None kabul etme girişi: doğru (ByValue) joker karakterleri kabul et: false</span><span class="sxs-lookup"><span data-stu-id="50f45-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f45-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f45-150">CommonParameters</span></span>
<span data-ttu-id="50f45-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50f45-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f45-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="50f45-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f45-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50f45-153">INPUTS</span></span>

### <span data-ttu-id="50f45-154">System. String</span><span class="sxs-lookup"><span data-stu-id="50f45-154">System.String</span></span>

### <span data-ttu-id="50f45-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="50f45-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="50f45-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50f45-156">OUTPUTS</span></span>

### <span data-ttu-id="50f45-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50f45-157">System.Boolean</span></span>

## <span data-ttu-id="50f45-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50f45-158">NOTES</span></span>

## <span data-ttu-id="50f45-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50f45-159">RELATED LINKS</span></span>
