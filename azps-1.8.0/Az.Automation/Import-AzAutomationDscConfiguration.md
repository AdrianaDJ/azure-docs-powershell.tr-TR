---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
ms.openlocfilehash: e1e7ed85a43492f4e00495df52f51c49712c4aff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761583"
---
# <span data-ttu-id="480db-101">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="480db-101">Import-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="480db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="480db-102">SYNOPSIS</span></span>
<span data-ttu-id="480db-103">DSC yapılandırmasını otomatikleştirme 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="480db-103">Imports a DSC configuration into Automation.</span></span>

## <span data-ttu-id="480db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="480db-104">SYNTAX</span></span>

```
Import-AzAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="480db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="480db-105">DESCRIPTION</span></span>
<span data-ttu-id="480db-106">**Import-AzAutomationDscConfiguration** cmdlet 'i, bir APS</span><span class="sxs-lookup"><span data-stu-id="480db-106">The **Import-AzAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="480db-107">Tek bir DSC yapılandırması içeren APS komut dosyasının yolunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="480db-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="480db-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="480db-108">EXAMPLES</span></span>

### <span data-ttu-id="480db-109">Örnek 1: DSC yapılandırmasını Otomasyonu içine aktarma</span><span class="sxs-lookup"><span data-stu-id="480db-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="480db-110">Bu komut client.ps1 adındaki dosyadaki DSC yapılandırmasını Contoso17 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="480db-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="480db-111">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="480db-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="480db-112">Var olan bir DSC yapılandırması varsa bu komut bunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="480db-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="480db-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="480db-113">PARAMETERS</span></span>

### <span data-ttu-id="480db-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="480db-114">-AutomationAccountName</span></span>
<span data-ttu-id="480db-115">Bu cmdlet 'in DSC yapılandırmasını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="480db-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="480db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480db-116">-DefaultProfile</span></span>
<span data-ttu-id="480db-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="480db-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="480db-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="480db-118">-Description</span></span>
<span data-ttu-id="480db-119">Bu cmdlet 'in içeri aktardığından yapılandırmanın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="480db-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="480db-120">-Force</span><span class="sxs-lookup"><span data-stu-id="480db-120">-Force</span></span>
<span data-ttu-id="480db-121">Bu cmdlet 'in Otomasyon 'daki mevcut bir DSC yapılandırmasını değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="480db-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="480db-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="480db-122">-LogVerbose</span></span>
<span data-ttu-id="480db-123">Bu cmdlet 'in bu DSC yapılandırmasının derleme işleri için ayrıntılı günlüğü açıp açamayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="480db-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="480db-124">Ayrıntılı günlüğü açmak veya $False kapatmak için $True değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="480db-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="480db-125">Yayımlanmış</span><span class="sxs-lookup"><span data-stu-id="480db-125">-Published</span></span>
<span data-ttu-id="480db-126">Bu cmdlet 'in, yayınlanmış durumundaki DSC yapılandırmasını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="480db-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="480db-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480db-127">-ResourceGroupName</span></span>
<span data-ttu-id="480db-128">Bu cmdlet 'in DSC yapılandırmasını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="480db-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="480db-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="480db-129">-SourcePath</span></span>
<span data-ttu-id="480db-130">Bu cmdlet 'in içeri aktardığından DSC yapılandırmasını içeren wps_2 betiğin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="480db-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="480db-131">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="480db-131">-Tags</span></span>
<span data-ttu-id="480db-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="480db-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="480db-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="480db-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="480db-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="480db-134">-Confirm</span></span>
<span data-ttu-id="480db-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="480db-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="480db-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="480db-136">-WhatIf</span></span>
<span data-ttu-id="480db-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="480db-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="480db-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="480db-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="480db-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480db-139">CommonParameters</span></span>
<span data-ttu-id="480db-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="480db-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480db-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="480db-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480db-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="480db-142">INPUTS</span></span>

### <span data-ttu-id="480db-143">System. String</span><span class="sxs-lookup"><span data-stu-id="480db-143">System.String</span></span>

### <span data-ttu-id="480db-144">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="480db-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="480db-145">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="480db-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="480db-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="480db-146">OUTPUTS</span></span>

### <span data-ttu-id="480db-147">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="480db-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="480db-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="480db-148">NOTES</span></span>

## <span data-ttu-id="480db-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="480db-149">RELATED LINKS</span></span>

[<span data-ttu-id="480db-150">Dışarı aktarma-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="480db-150">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="480db-151">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="480db-151">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)
