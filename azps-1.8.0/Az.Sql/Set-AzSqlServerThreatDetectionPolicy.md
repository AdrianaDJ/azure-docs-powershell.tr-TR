---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 8d58085aa55958e6e0fc9658d814d4bc05006fd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758747"
---
# <span data-ttu-id="6830e-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6830e-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="6830e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6830e-102">SYNOPSIS</span></span>
<span data-ttu-id="6830e-103">Bir sunucuda tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6830e-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="6830e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6830e-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6830e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6830e-105">DESCRIPTION</span></span>
<span data-ttu-id="6830e-106">**Set-AzSqlServerThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL Server 'da tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6830e-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="6830e-107">Bir sunucuda tehdit algılamasını etkinleştirmek için, bu sunucuda denetim ilkesi etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="6830e-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="6830e-108">Bu cmdlet 'i kullanmak için, sunucuyu tanımlayan *Resourcegroupname* ve ServerName parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6830e-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="6830e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6830e-109">EXAMPLES</span></span>

### <span data-ttu-id="6830e-110">Örnek 1: veritabanı için tehdit algılama ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="6830e-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="6830e-111">Bu komut, server01 adlı bir sunucuda tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6830e-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="6830e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6830e-112">PARAMETERS</span></span>

### <span data-ttu-id="6830e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6830e-113">-DefaultProfile</span></span>
<span data-ttu-id="6830e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6830e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6830e-115">-Eda</span><span class="sxs-lookup"><span data-stu-id="6830e-115">-EmailAdmins</span></span>
<span data-ttu-id="6830e-116">Tehdit algılama ilkesinin e-posta kullanarak yöneticilere mı ait olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6830e-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="6830e-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="6830e-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="6830e-118">İlkeden dışlanacak algılama türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6830e-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="6830e-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6830e-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6830e-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="6830e-120">Sql_Injection</span></span>
- <span data-ttu-id="6830e-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="6830e-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="6830e-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="6830e-122">Access_Anomaly</span></span>
- <span data-ttu-id="6830e-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6830e-123">None</span></span>

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

### <span data-ttu-id="6830e-124">-Notificationrecipientşeması ILS</span><span class="sxs-lookup"><span data-stu-id="6830e-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="6830e-125">İlkenin uyarıları gönderdiği e-posta adreslerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6830e-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="6830e-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6830e-126">-PassThru</span></span>
<span data-ttu-id="6830e-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6830e-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6830e-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6830e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6830e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6830e-129">-ResourceGroupName</span></span>
<span data-ttu-id="6830e-130">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6830e-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="6830e-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6830e-131">-RetentionInDays</span></span>
<span data-ttu-id="6830e-132">Denetim günlükleri için bekletme günü sayısı</span><span class="sxs-lookup"><span data-stu-id="6830e-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="6830e-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6830e-133">-ServerName</span></span>
<span data-ttu-id="6830e-134">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6830e-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6830e-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6830e-135">-StorageAccountName</span></span>
<span data-ttu-id="6830e-136">Kullanılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6830e-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="6830e-137">Joker karakterlere izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="6830e-137">Wildcards are not permitted.</span></span> <span data-ttu-id="6830e-138">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="6830e-138">This parameter is not required.</span></span> <span data-ttu-id="6830e-139">Bu parametre sağlanmadıysa cmdlet, veritabanının tehdit algılama ilkesinin bir parçası olarak daha önce tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="6830e-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="6830e-140">Bir veritabanı algılama ilkesi ilk kez tanımlandıysa ve bu parametre sağlanmadıysa cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="6830e-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="6830e-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="6830e-141">-Confirm</span></span>
<span data-ttu-id="6830e-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6830e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6830e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6830e-143">-WhatIf</span></span>
<span data-ttu-id="6830e-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6830e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6830e-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6830e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6830e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6830e-146">CommonParameters</span></span>
<span data-ttu-id="6830e-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6830e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6830e-148">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6830e-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6830e-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6830e-149">INPUTS</span></span>

### <span data-ttu-id="6830e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6830e-150">System.String</span></span>

### <span data-ttu-id="6830e-151">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="6830e-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6830e-152">Microsoft. Azure. Commands. Sql. ThreatDetection. model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="6830e-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="6830e-153">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="6830e-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6830e-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6830e-154">OUTPUTS</span></span>

### <span data-ttu-id="6830e-155">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="6830e-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="6830e-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6830e-156">NOTES</span></span>

## <span data-ttu-id="6830e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6830e-157">RELATED LINKS</span></span>

[<span data-ttu-id="6830e-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6830e-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="6830e-159">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6830e-159">Remove-AzSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="6830e-160">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="6830e-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
