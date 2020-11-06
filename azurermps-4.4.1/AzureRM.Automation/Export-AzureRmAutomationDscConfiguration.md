---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: ed35cf910dd0bf51803b6a38edc90a93f5411520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587002"
---
# <span data-ttu-id="fd266-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd266-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="fd266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd266-102">SYNOPSIS</span></span>
<span data-ttu-id="fd266-103">Bir DSC yapılandırmasını otomasyondan yerel dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="fd266-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd266-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd266-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd266-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd266-105">DESCRIPTION</span></span>
<span data-ttu-id="fd266-106">**Export-AzureRmAutomationDscConfiguration** cmdlet 'i, bir APS Istenen durum yapılandırma (DSC) yapılandırmasını Azure Otomasyonu 'ndan yerel dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="fd266-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="fd266-107">Dışarı aktarılan dosyanın. ps1 dosya adı uzantısı vardır.</span><span class="sxs-lookup"><span data-stu-id="fd266-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="fd266-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd266-108">EXAMPLES</span></span>

### <span data-ttu-id="fd266-109">Örnek 1: DSC yapılandırmasının yayımlanmış sürümünü dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="fd266-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="fd266-110">Bu komut, bir DSC yapılandırmasının yayımlanan sürümünü Otomasyon 'daki belirtilen klasöre (Masaüstü) dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="fd266-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="fd266-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd266-111">PARAMETERS</span></span>

### <span data-ttu-id="fd266-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd266-112">-AutomationAccountName</span></span>
<span data-ttu-id="fd266-113">Bu cmdlet 'in dışarı aktardığı DSC 'yi içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd266-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="fd266-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fd266-114">-Force</span></span>
<span data-ttu-id="fd266-115">Bu cmdlet 'in varolan bir yerel dosyayı aynı ada sahip yeni bir dosyayla değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd266-115">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="fd266-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd266-116">-Name</span></span>
<span data-ttu-id="fd266-117">Bu cmdlet 'in dışarı aktardığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd266-117">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd266-118">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="fd266-118">-OutputFolder</span></span>
<span data-ttu-id="fd266-119">Bu cmdlet 'in DSC yapılandırmasını dışarı aktardığı çıkış klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd266-119">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="fd266-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd266-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd266-121">Bu cmdlet 'in DSC yapılandırmasını dışarı aktardığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd266-121">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="fd266-122">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="fd266-122">-Slot</span></span>
<span data-ttu-id="fd266-123">Bu cmdlet 'in DSC yapılandırmasının hangi sürümünü dışarı aktaracağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd266-123">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="fd266-124">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="fd266-124">Valid values are:</span></span> 

- <span data-ttu-id="fd266-125">Lar</span><span class="sxs-lookup"><span data-stu-id="fd266-125">Draft</span></span>
- <span data-ttu-id="fd266-126">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="fd266-126">Published</span></span> 

<span data-ttu-id="fd266-127">Varsayılan değer yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="fd266-127">The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd266-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd266-128">-Confirm</span></span>
<span data-ttu-id="fd266-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd266-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd266-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd266-130">-WhatIf</span></span>
<span data-ttu-id="fd266-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd266-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd266-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd266-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd266-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd266-133">-DefaultProfile</span></span>
<span data-ttu-id="fd266-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd266-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd266-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd266-135">CommonParameters</span></span>
<span data-ttu-id="fd266-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd266-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd266-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd266-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd266-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd266-138">INPUTS</span></span>

## <span data-ttu-id="fd266-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd266-139">OUTPUTS</span></span>

### <span data-ttu-id="fd266-140">System. ıO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="fd266-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="fd266-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd266-141">NOTES</span></span>

## <span data-ttu-id="fd266-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd266-142">RELATED LINKS</span></span>

[<span data-ttu-id="fd266-143">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd266-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="fd266-144">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd266-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


