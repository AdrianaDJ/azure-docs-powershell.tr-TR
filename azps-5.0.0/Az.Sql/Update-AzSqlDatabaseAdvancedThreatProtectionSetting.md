---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276956"
---
# <span data-ttu-id="83d24-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="83d24-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="83d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d24-102">SYNOPSIS</span></span>
<span data-ttu-id="83d24-103">Veritabanında Gelişmiş tehdit koruması ayarlarını yapar.</span><span class="sxs-lookup"><span data-stu-id="83d24-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="83d24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83d24-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d24-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83d24-105">DESCRIPTION</span></span>
<span data-ttu-id="83d24-106">**Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet 'ı, Azure SQL veritabanında gelişmiş bir tehdit koruması ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83d24-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="83d24-107">Veritabanında Gelişmiş tehdit korumasını etkinleştirmek için, bu veritabanında denetim ayarları etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="83d24-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="83d24-108">Bu cmdlet 'i kullanmak için, veritabanını tanımlayacak *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="83d24-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="83d24-109">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="83d24-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="83d24-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83d24-110">EXAMPLES</span></span>

### <span data-ttu-id="83d24-111">Örnek 1: veritabanı için Gelişmiş tehdit koruması ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="83d24-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="83d24-112">Bu komut, server01 adındaki sunucudaki Database01 adındaki veritabanı için Gelişmiş tehdit koruması ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83d24-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="83d24-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83d24-113">PARAMETERS</span></span>

### <span data-ttu-id="83d24-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83d24-114">-DatabaseName</span></span>
<span data-ttu-id="83d24-115">Ayarların ayarlandığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83d24-115">Specifies the name of the database where the settings is set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d24-116">-DefaultProfile</span></span>
<span data-ttu-id="83d24-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="83d24-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83d24-118">-Eda</span><span class="sxs-lookup"><span data-stu-id="83d24-118">-EmailAdmins</span></span>
<span data-ttu-id="83d24-119">Gelişmiş tehdit koruması ayarlarının e-posta kullanarak yöneticilere mı ait olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="83d24-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="83d24-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="83d24-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="83d24-121">Ayarlardan çıkarılacak algılama türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83d24-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="83d24-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="83d24-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="83d24-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="83d24-123">Sql_Injection</span></span> 
- <span data-ttu-id="83d24-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="83d24-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="83d24-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="83d24-125">Access_Anomaly</span></span> 
- <span data-ttu-id="83d24-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="83d24-126">None</span></span>

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

### <span data-ttu-id="83d24-127">-Notificationrecipientşeması ILS</span><span class="sxs-lookup"><span data-stu-id="83d24-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="83d24-128">Ayarların uyarı gönderdiği e-posta adreslerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83d24-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="83d24-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="83d24-129">-PassThru</span></span>
<span data-ttu-id="83d24-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="83d24-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83d24-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="83d24-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83d24-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d24-132">-ResourceGroupName</span></span>
<span data-ttu-id="83d24-133">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83d24-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="83d24-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="83d24-134">-RetentionInDays</span></span>
<span data-ttu-id="83d24-135">Denetim günlükleri için bekletme günü sayısı</span><span class="sxs-lookup"><span data-stu-id="83d24-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="83d24-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83d24-136">-ServerName</span></span>
<span data-ttu-id="83d24-137">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83d24-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="83d24-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="83d24-138">-StorageAccountName</span></span>
<span data-ttu-id="83d24-139">Kullanılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83d24-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="83d24-140">Joker karakterlere izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="83d24-140">Wildcards are not permitted.</span></span> <span data-ttu-id="83d24-141">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="83d24-141">This parameter is not required.</span></span> <span data-ttu-id="83d24-142">Bu parametre sağlanmadıysa cmdlet, veritabanının Gelişmiş tehdit koruması ayarlarının bir parçası olarak daha önce tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="83d24-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="83d24-143">Bu, veritabanı Gelişmiş tehdit koruması ayarları ilk kez tanımlandıysa ve bu parametre sağlanmadıysa cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="83d24-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="83d24-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="83d24-144">-Confirm</span></span>
<span data-ttu-id="83d24-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83d24-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d24-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d24-146">-WhatIf</span></span>
<span data-ttu-id="83d24-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83d24-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d24-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83d24-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d24-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d24-149">CommonParameters</span></span>
<span data-ttu-id="83d24-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83d24-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d24-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83d24-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d24-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83d24-152">INPUTS</span></span>

### <span data-ttu-id="83d24-153">System. String</span><span class="sxs-lookup"><span data-stu-id="83d24-153">System.String</span></span>

### <span data-ttu-id="83d24-154">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="83d24-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="83d24-155">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="83d24-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="83d24-156">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="83d24-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="83d24-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83d24-157">OUTPUTS</span></span>

### <span data-ttu-id="83d24-158">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="83d24-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="83d24-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83d24-159">NOTES</span></span>

## <span data-ttu-id="83d24-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83d24-160">RELATED LINKS</span></span>

[<span data-ttu-id="83d24-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="83d24-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="83d24-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="83d24-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="83d24-163">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="83d24-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


