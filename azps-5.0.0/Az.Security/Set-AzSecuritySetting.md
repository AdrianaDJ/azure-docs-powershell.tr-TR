---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276190"
---
# <span data-ttu-id="dacf5-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="dacf5-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="dacf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dacf5-102">SYNOPSIS</span></span>
<span data-ttu-id="dacf5-103">Azure Güvenlik Merkezi 'nde güvenlik ayarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="dacf5-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="dacf5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dacf5-104">SYNTAX</span></span>

### <span data-ttu-id="dacf5-105">Genelkapsam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dacf5-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dacf5-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="dacf5-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dacf5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dacf5-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dacf5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dacf5-108">DESCRIPTION</span></span>
<span data-ttu-id="dacf5-109">Set-AzSecuritySetting cmdlet 'i, Azure Güvenlik Merkezi 'nde belirli bir güvenlik ayarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dacf5-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="dacf5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dacf5-110">EXAMPLES</span></span>

### <span data-ttu-id="dacf5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dacf5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="dacf5-112">Bir MCAS veri dışarı aktarma ayarını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="dacf5-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="dacf5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dacf5-113">PARAMETERS</span></span>

### <span data-ttu-id="dacf5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacf5-114">-DefaultProfile</span></span>
<span data-ttu-id="dacf5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dacf5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dacf5-116">Özellikli</span><span class="sxs-lookup"><span data-stu-id="dacf5-116">-Enabled</span></span>
<span data-ttu-id="dacf5-117">Ayarı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="dacf5-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacf5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dacf5-118">-InputObject</span></span>
<span data-ttu-id="dacf5-119">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dacf5-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dacf5-120">-Settingtür</span><span class="sxs-lookup"><span data-stu-id="dacf5-120">-SettingKind</span></span>
<span data-ttu-id="dacf5-121">Ayar türü.</span><span class="sxs-lookup"><span data-stu-id="dacf5-121">Setting kind.</span></span> <span data-ttu-id="dacf5-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="dacf5-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacf5-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="dacf5-123">-SettingName</span></span>
<span data-ttu-id="dacf5-124">Ayar adı.</span><span class="sxs-lookup"><span data-stu-id="dacf5-124">Setting name.</span></span> <span data-ttu-id="dacf5-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="dacf5-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacf5-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="dacf5-126">-Confirm</span></span>
<span data-ttu-id="dacf5-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dacf5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dacf5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dacf5-128">-WhatIf</span></span>
<span data-ttu-id="dacf5-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dacf5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dacf5-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dacf5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dacf5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacf5-131">CommonParameters</span></span>
<span data-ttu-id="dacf5-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dacf5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacf5-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dacf5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacf5-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dacf5-134">INPUTS</span></span>

### <span data-ttu-id="dacf5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dacf5-135">System.String</span></span>
### <span data-ttu-id="dacf5-136">Microsoft. Azure. Commands. Security. model. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="dacf5-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="dacf5-137">Microsoft. Azure. Commands. Security. model. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="dacf5-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="dacf5-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dacf5-138">System.Boolean</span></span>

## <span data-ttu-id="dacf5-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dacf5-139">OUTPUTS</span></span>

### <span data-ttu-id="dacf5-140">Microsoft. Azure. Commands. Security. model. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="dacf5-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="dacf5-141">Microsoft. Azure. Commands. Security. model. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="dacf5-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="dacf5-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dacf5-142">NOTES</span></span>

## <span data-ttu-id="dacf5-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dacf5-143">RELATED LINKS</span></span>
