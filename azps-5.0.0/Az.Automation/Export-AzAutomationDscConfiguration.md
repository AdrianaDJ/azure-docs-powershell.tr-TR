---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324013"
---
# <span data-ttu-id="6130f-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6130f-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="6130f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6130f-102">SYNOPSIS</span></span>
<span data-ttu-id="6130f-103">Bir DSC yapılandırmasını otomasyondan yerel dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="6130f-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="6130f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6130f-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6130f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6130f-105">DESCRIPTION</span></span>
<span data-ttu-id="6130f-106">**Export-AzAutomationDscConfiguration** cmdlet 'i, bir APS Istenen durum yapılandırma (DSC) yapılandırmasını Azure Otomasyonu 'ndan yerel dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="6130f-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="6130f-107">Dışarı aktarılan dosyanın. ps1 dosya adı uzantısı vardır.</span><span class="sxs-lookup"><span data-stu-id="6130f-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="6130f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6130f-108">EXAMPLES</span></span>

### <span data-ttu-id="6130f-109">Örnek 1: DSC yapılandırmasının yayımlanmış sürümünü dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="6130f-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="6130f-110">Bu komut, bir DSC yapılandırmasının yayımlanan sürümünü Otomasyon 'daki belirtilen klasöre (Masaüstü) dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="6130f-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="6130f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6130f-111">PARAMETERS</span></span>

### <span data-ttu-id="6130f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6130f-112">-AutomationAccountName</span></span>
<span data-ttu-id="6130f-113">Bu cmdlet 'in dışarı aktardığı DSC 'yi içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6130f-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="6130f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6130f-114">-DefaultProfile</span></span>
<span data-ttu-id="6130f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6130f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6130f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6130f-116">-Force</span></span>
<span data-ttu-id="6130f-117">Bu cmdlet 'in varolan bir yerel dosyayı aynı ada sahip yeni bir dosyayla değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6130f-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="6130f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6130f-118">-Name</span></span>
<span data-ttu-id="6130f-119">Bu cmdlet 'in dışarı aktardığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6130f-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="6130f-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="6130f-120">-OutputFolder</span></span>
<span data-ttu-id="6130f-121">Bu cmdlet 'in DSC yapılandırmasını dışarı aktardığı çıkış klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6130f-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="6130f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6130f-122">-ResourceGroupName</span></span>
<span data-ttu-id="6130f-123">Bu cmdlet 'in DSC yapılandırmasını dışarı aktardığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6130f-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="6130f-124">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="6130f-124">-Slot</span></span>
<span data-ttu-id="6130f-125">Bu cmdlet 'in DSC yapılandırmasının hangi sürümünü dışarı aktaracağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6130f-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="6130f-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="6130f-126">Valid values are:</span></span> 
- <span data-ttu-id="6130f-127">Lar</span><span class="sxs-lookup"><span data-stu-id="6130f-127">Draft</span></span>
- <span data-ttu-id="6130f-128">Yayımlandı varsayılan değer yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="6130f-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="6130f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6130f-129">-Confirm</span></span>
<span data-ttu-id="6130f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6130f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6130f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6130f-131">-WhatIf</span></span>
<span data-ttu-id="6130f-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6130f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6130f-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6130f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6130f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6130f-134">CommonParameters</span></span>
<span data-ttu-id="6130f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6130f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6130f-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6130f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6130f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6130f-137">INPUTS</span></span>

### <span data-ttu-id="6130f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6130f-138">System.String</span></span>

## <span data-ttu-id="6130f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6130f-139">OUTPUTS</span></span>

### <span data-ttu-id="6130f-140">System. ıO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="6130f-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="6130f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6130f-141">NOTES</span></span>

## <span data-ttu-id="6130f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6130f-142">RELATED LINKS</span></span>

[<span data-ttu-id="6130f-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6130f-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="6130f-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6130f-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


