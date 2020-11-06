---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591185"
---
# <span data-ttu-id="cadd0-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cadd0-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="cadd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cadd0-102">SYNOPSIS</span></span>
<span data-ttu-id="cadd0-103">DSC yapılandırmasını otomatikleştirme 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="cadd0-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cadd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cadd0-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cadd0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cadd0-105">DESCRIPTION</span></span>
<span data-ttu-id="cadd0-106">**Import-AzureRmAutomationDscConfiguration** cmdlet 'i, bir APS</span><span class="sxs-lookup"><span data-stu-id="cadd0-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="cadd0-107">Tek bir DSC yapılandırması içeren APS komut dosyasının yolunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="cadd0-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="cadd0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cadd0-108">EXAMPLES</span></span>

### <span data-ttu-id="cadd0-109">Örnek 1: DSC yapılandırmasını Otomasyonu içine aktarma</span><span class="sxs-lookup"><span data-stu-id="cadd0-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="cadd0-110">Bu komut client.ps1 adındaki dosyadaki DSC yapılandırmasını Contoso17 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="cadd0-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="cadd0-111">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="cadd0-112">Var olan bir DSC yapılandırması varsa bu komut bunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="cadd0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cadd0-113">PARAMETERS</span></span>

### <span data-ttu-id="cadd0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cadd0-114">-AutomationAccountName</span></span>
<span data-ttu-id="cadd0-115">Bu cmdlet 'in DSC yapılandırmasını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadd0-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="cadd0-116">-Description</span></span>
<span data-ttu-id="cadd0-117">Bu cmdlet 'in içeri aktardığından yapılandırmanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="cadd0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cadd0-118">-Force</span></span>
<span data-ttu-id="cadd0-119">Bu cmdlet 'in Otomasyon 'daki mevcut bir DSC yapılandırmasını değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="cadd0-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="cadd0-120">-LogVerbose</span></span>
<span data-ttu-id="cadd0-121">Bu cmdlet 'in bu DSC yapılandırmasının derleme işleri için ayrıntılı günlüğü açıp açamayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="cadd0-122">Ayrıntılı günlüğü açmak veya $False kapatmak için $True değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="cadd0-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadd0-123">Yayımlanmış</span><span class="sxs-lookup"><span data-stu-id="cadd0-123">-Published</span></span>
<span data-ttu-id="cadd0-124">Bu cmdlet 'in, yayınlanmış durumundaki DSC yapılandırmasını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="cadd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="cadd0-126">Bu cmdlet 'in DSC yapılandırmasını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadd0-127">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="cadd0-127">-SourcePath</span></span>
<span data-ttu-id="cadd0-128">Bu cmdlet 'in içeri aktardığından DSC yapılandırmasını içeren wps_2 betiğin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadd0-129">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="cadd0-129">-Tags</span></span>
<span data-ttu-id="cadd0-130">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="cadd0-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cadd0-131">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="cadd0-131">For example:</span></span>

<span data-ttu-id="cadd0-132">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="cadd0-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadd0-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="cadd0-133">-Confirm</span></span>
<span data-ttu-id="cadd0-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cadd0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cadd0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cadd0-135">-WhatIf</span></span>
<span data-ttu-id="cadd0-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cadd0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cadd0-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cadd0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cadd0-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadd0-138">-DefaultProfile</span></span>
<span data-ttu-id="cadd0-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cadd0-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cadd0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadd0-140">CommonParameters</span></span>
<span data-ttu-id="cadd0-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cadd0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadd0-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cadd0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadd0-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cadd0-143">INPUTS</span></span>

## <span data-ttu-id="cadd0-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cadd0-144">OUTPUTS</span></span>

### <span data-ttu-id="cadd0-145">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cadd0-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="cadd0-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cadd0-146">NOTES</span></span>

## <span data-ttu-id="cadd0-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cadd0-147">RELATED LINKS</span></span>

[<span data-ttu-id="cadd0-148">Dışarı aktarma-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cadd0-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="cadd0-149">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cadd0-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
