---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 3ec370f0e4865ed5695e4f0890f99b50709e9ad8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937945"
---
# <span data-ttu-id="cf51e-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cf51e-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cf51e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf51e-102">SYNOPSIS</span></span>
<span data-ttu-id="cf51e-103">Sunucuda Gelişmiş tehdit koruması ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf51e-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="cf51e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf51e-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf51e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf51e-105">DESCRIPTION</span></span>
<span data-ttu-id="cf51e-106">**Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet 'i, BIR Azure SQL Server 'da Gelişmiş tehdit koruması ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf51e-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="cf51e-107">Sunucuda Gelişmiş tehdit korumasını etkinleştirmek için, bu sunucuda denetim ayarları etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="cf51e-108">Bu cmdlet 'i kullanmak için, sunucuyu tanımlayan *Resourcegroupname* ve ServerName parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="cf51e-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="cf51e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf51e-109">EXAMPLES</span></span>

### <span data-ttu-id="cf51e-110">Örnek 1: veritabanı için Gelişmiş tehdit koruması ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="cf51e-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="cf51e-111">Bu komut, server01 adlı bir sunucunun Gelişmiş tehdit koruması ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf51e-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="cf51e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf51e-112">PARAMETERS</span></span>

### <span data-ttu-id="cf51e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf51e-113">-DefaultProfile</span></span>
<span data-ttu-id="cf51e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cf51e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf51e-115">-Eda</span><span class="sxs-lookup"><span data-stu-id="cf51e-115">-EmailAdmins</span></span>
<span data-ttu-id="cf51e-116">Gelişmiş tehdit koruması ayarlarının e-posta kullanarak yöneticilere mı ait olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="cf51e-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="cf51e-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="cf51e-118">Ayarlardan çıkarılacak algılama türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="cf51e-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cf51e-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf51e-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="cf51e-120">Sql_Injection</span></span>
- <span data-ttu-id="cf51e-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="cf51e-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="cf51e-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="cf51e-122">Access_Anomaly</span></span>
- <span data-ttu-id="cf51e-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cf51e-123">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf51e-124">-Notificationrecipientşeması ILS</span><span class="sxs-lookup"><span data-stu-id="cf51e-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="cf51e-125">Ayarların uyarı gönderdiği e-posta adreslerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="cf51e-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cf51e-126">-PassThru</span></span>
<span data-ttu-id="cf51e-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf51e-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf51e-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cf51e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf51e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf51e-129">-ResourceGroupName</span></span>
<span data-ttu-id="cf51e-130">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="cf51e-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cf51e-131">-RetentionInDays</span></span>
<span data-ttu-id="cf51e-132">Denetim günlükleri için bekletme günü sayısı</span><span class="sxs-lookup"><span data-stu-id="cf51e-132">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf51e-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cf51e-133">-ServerName</span></span>
<span data-ttu-id="cf51e-134">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-134">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf51e-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cf51e-135">-StorageAccountName</span></span>
<span data-ttu-id="cf51e-136">Kullanılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="cf51e-137">Joker karakterlere izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="cf51e-137">Wildcards are not permitted.</span></span> <span data-ttu-id="cf51e-138">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-138">This parameter is not required.</span></span> <span data-ttu-id="cf51e-139">Bu parametre sağlanmadıysa cmdlet, veritabanının Gelişmiş tehdit koruması ayarlarının bir parçası olarak daha önce tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="cf51e-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="cf51e-140">Bu, veritabanı tehdit algılama ayarlarının tanımlanması durumunda ve bu parametre sağlanmadıysa cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="cf51e-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="cf51e-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf51e-141">-Confirm</span></span>
<span data-ttu-id="cf51e-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf51e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf51e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf51e-143">-WhatIf</span></span>
<span data-ttu-id="cf51e-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf51e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf51e-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf51e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf51e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf51e-146">CommonParameters</span></span>
<span data-ttu-id="cf51e-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf51e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf51e-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cf51e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf51e-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf51e-149">INPUTS</span></span>

### <span data-ttu-id="cf51e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cf51e-150">System.String</span></span>

### <span data-ttu-id="cf51e-151">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf51e-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cf51e-152">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="cf51e-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="cf51e-153">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf51e-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cf51e-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf51e-154">OUTPUTS</span></span>

### <span data-ttu-id="cf51e-155">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="cf51e-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="cf51e-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf51e-156">NOTES</span></span>

## <span data-ttu-id="cf51e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf51e-157">RELATED LINKS</span></span>

[<span data-ttu-id="cf51e-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="cf51e-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="cf51e-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="cf51e-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="cf51e-160">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="cf51e-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
