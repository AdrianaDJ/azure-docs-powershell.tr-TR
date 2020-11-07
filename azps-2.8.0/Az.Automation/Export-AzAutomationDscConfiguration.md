---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 8abd6859054245c6265cc32695fa56168aabd1c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753358"
---
# <span data-ttu-id="63b93-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63b93-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="63b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63b93-102">SYNOPSIS</span></span>
<span data-ttu-id="63b93-103">Bir DSC yapılandırmasını otomasyondan yerel dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="63b93-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="63b93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63b93-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63b93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63b93-105">DESCRIPTION</span></span>
<span data-ttu-id="63b93-106">**Export-AzAutomationDscConfiguration** cmdlet 'i, bir APS Istenen durum yapılandırma (DSC) yapılandırmasını Azure Otomasyonu 'ndan yerel dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="63b93-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="63b93-107">Dışarı aktarılan dosyanın. ps1 dosya adı uzantısı vardır.</span><span class="sxs-lookup"><span data-stu-id="63b93-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="63b93-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63b93-108">EXAMPLES</span></span>

### <span data-ttu-id="63b93-109">Örnek 1: DSC yapılandırmasının yayımlanmış sürümünü dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="63b93-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="63b93-110">Bu komut, bir DSC yapılandırmasının yayımlanan sürümünü Otomasyon 'daki belirtilen klasöre (Masaüstü) dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="63b93-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="63b93-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63b93-111">PARAMETERS</span></span>

### <span data-ttu-id="63b93-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="63b93-112">-AutomationAccountName</span></span>
<span data-ttu-id="63b93-113">Bu cmdlet 'in dışarı aktardığı DSC 'yi içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63b93-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="63b93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63b93-114">-DefaultProfile</span></span>
<span data-ttu-id="63b93-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="63b93-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63b93-116">-Force</span><span class="sxs-lookup"><span data-stu-id="63b93-116">-Force</span></span>
<span data-ttu-id="63b93-117">Bu cmdlet 'in varolan bir yerel dosyayı aynı ada sahip yeni bir dosyayla değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63b93-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="63b93-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="63b93-118">-Name</span></span>
<span data-ttu-id="63b93-119">Bu cmdlet 'in dışarı aktardığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63b93-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="63b93-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="63b93-120">-OutputFolder</span></span>
<span data-ttu-id="63b93-121">Bu cmdlet 'in DSC yapılandırmasını dışarı aktardığı çıkış klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="63b93-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="63b93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63b93-122">-ResourceGroupName</span></span>
<span data-ttu-id="63b93-123">Bu cmdlet 'in DSC yapılandırmasını dışarı aktardığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63b93-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="63b93-124">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="63b93-124">-Slot</span></span>
<span data-ttu-id="63b93-125">Bu cmdlet 'in DSC yapılandırmasının hangi sürümünü dışarı aktaracağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63b93-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="63b93-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="63b93-126">Valid values are:</span></span> 
- <span data-ttu-id="63b93-127">Lar</span><span class="sxs-lookup"><span data-stu-id="63b93-127">Draft</span></span>
- <span data-ttu-id="63b93-128">Yayımlandı varsayılan değer yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="63b93-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="63b93-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="63b93-129">-Confirm</span></span>
<span data-ttu-id="63b93-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63b93-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63b93-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63b93-131">-WhatIf</span></span>
<span data-ttu-id="63b93-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63b93-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63b93-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63b93-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63b93-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63b93-134">CommonParameters</span></span>
<span data-ttu-id="63b93-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63b93-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63b93-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63b93-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63b93-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63b93-137">INPUTS</span></span>

### <span data-ttu-id="63b93-138">System. String</span><span class="sxs-lookup"><span data-stu-id="63b93-138">System.String</span></span>

## <span data-ttu-id="63b93-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63b93-139">OUTPUTS</span></span>

### <span data-ttu-id="63b93-140">System. ıO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="63b93-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="63b93-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63b93-141">NOTES</span></span>

## <span data-ttu-id="63b93-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63b93-142">RELATED LINKS</span></span>

[<span data-ttu-id="63b93-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63b93-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="63b93-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="63b93-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


