---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e8d7cfcf595d7dd445d66865d922676c96b7e6d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586829"
---
# <span data-ttu-id="7e755-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e755-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="7e755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e755-102">SYNOPSIS</span></span>
<span data-ttu-id="7e755-103">DSC yapılandırmasını otomatikleştirme 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="7e755-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e755-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e755-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e755-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e755-105">DESCRIPTION</span></span>
<span data-ttu-id="7e755-106">**Import-AzureRmAutomationDscConfiguration** cmdlet 'i, bir APS</span><span class="sxs-lookup"><span data-stu-id="7e755-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="7e755-107">Tek bir DSC yapılandırması içeren APS komut dosyasının yolunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="7e755-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="7e755-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e755-108">EXAMPLES</span></span>

### <span data-ttu-id="7e755-109">Örnek 1: DSC yapılandırmasını Otomasyonu içine aktarma</span><span class="sxs-lookup"><span data-stu-id="7e755-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="7e755-110">Bu komut client.ps1 adındaki dosyadaki DSC yapılandırmasını Contoso17 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="7e755-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="7e755-111">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e755-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="7e755-112">Var olan bir DSC yapılandırması varsa bu komut bunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7e755-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="7e755-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e755-113">PARAMETERS</span></span>

### <span data-ttu-id="7e755-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7e755-114">-AutomationAccountName</span></span>
<span data-ttu-id="7e755-115">Bu cmdlet 'in DSC yapılandırmasını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e755-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e755-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e755-116">-DefaultProfile</span></span>
<span data-ttu-id="7e755-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7e755-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e755-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7e755-118">-Description</span></span>
<span data-ttu-id="7e755-119">Bu cmdlet 'in içeri aktardığından yapılandırmanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e755-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="7e755-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7e755-120">-Force</span></span>
<span data-ttu-id="7e755-121">Bu cmdlet 'in Otomasyon 'daki mevcut bir DSC yapılandırmasını değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e755-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="7e755-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="7e755-122">-LogVerbose</span></span>
<span data-ttu-id="7e755-123">Bu cmdlet 'in bu DSC yapılandırmasının derleme işleri için ayrıntılı günlüğü açıp açamayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e755-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="7e755-124">Ayrıntılı günlüğü açmak veya $False kapatmak için $True değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7e755-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e755-125">Yayımlanmış</span><span class="sxs-lookup"><span data-stu-id="7e755-125">-Published</span></span>
<span data-ttu-id="7e755-126">Bu cmdlet 'in, yayınlanmış durumundaki DSC yapılandırmasını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e755-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="7e755-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e755-127">-ResourceGroupName</span></span>
<span data-ttu-id="7e755-128">Bu cmdlet 'in DSC yapılandırmasını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e755-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e755-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="7e755-129">-SourcePath</span></span>
<span data-ttu-id="7e755-130">Bu cmdlet 'in içeri aktardığından DSC yapılandırmasını içeren wps_2 betiğin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e755-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e755-131">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="7e755-131">-Tags</span></span>
<span data-ttu-id="7e755-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="7e755-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7e755-133">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="7e755-133">For example:</span></span>

<span data-ttu-id="7e755-134">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="7e755-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e755-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e755-135">-Confirm</span></span>
<span data-ttu-id="7e755-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e755-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e755-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e755-137">-WhatIf</span></span>
<span data-ttu-id="7e755-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e755-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e755-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e755-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e755-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e755-140">CommonParameters</span></span>
<span data-ttu-id="7e755-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e755-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e755-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e755-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e755-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e755-143">INPUTS</span></span>

### <span data-ttu-id="7e755-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7e755-144">None</span></span>
<span data-ttu-id="7e755-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7e755-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e755-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e755-146">OUTPUTS</span></span>

### <span data-ttu-id="7e755-147">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e755-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="7e755-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e755-148">NOTES</span></span>

## <span data-ttu-id="7e755-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e755-149">RELATED LINKS</span></span>

[<span data-ttu-id="7e755-150">Dışarı aktarma-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e755-150">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="7e755-151">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e755-151">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
