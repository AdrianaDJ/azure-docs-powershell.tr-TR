---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 7c71e9390ca28b48127a2f977e04eba645ae962f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594983"
---
# <span data-ttu-id="971a1-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="971a1-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="971a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="971a1-102">SYNOPSIS</span></span>
<span data-ttu-id="971a1-103">Bir sunucuda tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="971a1-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="971a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="971a1-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="971a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="971a1-105">DESCRIPTION</span></span>
<span data-ttu-id="971a1-106">**Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL Server 'da tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="971a1-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="971a1-107">Bir sunucuda tehdit algılamasını etkinleştirmek için, bu sunucuda denetim ilkesi etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="971a1-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="971a1-108">Bu cmdlet 'i kullanmak için, sunucuyu tanımlayan *Resourcegroupname* ve ServerName parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="971a1-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="971a1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="971a1-109">EXAMPLES</span></span>

### <span data-ttu-id="971a1-110">Örnek 1: veritabanı için tehdit algılama ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="971a1-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="971a1-111">Bu komut, server01 adlı bir sunucuda tehdit algılama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="971a1-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="971a1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="971a1-112">PARAMETERS</span></span>

### <span data-ttu-id="971a1-113">-Eda</span><span class="sxs-lookup"><span data-stu-id="971a1-113">-EmailAdmins</span></span>
<span data-ttu-id="971a1-114">Tehdit algılama ilkesinin e-posta kullanarak yöneticilere mı ait olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="971a1-114">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="971a1-115">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="971a1-115">-ExcludedDetectionType</span></span>
<span data-ttu-id="971a1-116">İlkeden dışlanacak algılama türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="971a1-116">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="971a1-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="971a1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="971a1-118">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="971a1-118">Sql_Injection</span></span>
- <span data-ttu-id="971a1-119">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="971a1-119">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="971a1-120">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="971a1-120">Access_Anomaly</span></span>
- <span data-ttu-id="971a1-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="971a1-121">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971a1-122">-Notificationrecipientşeması ILS</span><span class="sxs-lookup"><span data-stu-id="971a1-122">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="971a1-123">İlkenin uyarıları gönderdiği e-posta adreslerinin noktalı virgülle ayrılmış listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="971a1-123">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="971a1-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="971a1-124">-PassThru</span></span>
<span data-ttu-id="971a1-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="971a1-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="971a1-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="971a1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="971a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="971a1-128">Sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="971a1-128">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="971a1-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="971a1-129">-RetentionInDays</span></span>
<span data-ttu-id="971a1-130">Denetim günlükleri için bekletme günü sayısı</span><span class="sxs-lookup"><span data-stu-id="971a1-130">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="971a1-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="971a1-131">-ServerName</span></span>
<span data-ttu-id="971a1-132">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="971a1-132">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="971a1-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="971a1-133">-StorageAccountName</span></span>
<span data-ttu-id="971a1-134">Kullanılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="971a1-134">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="971a1-135">Joker karakterlere izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="971a1-135">Wildcards are not permitted.</span></span> <span data-ttu-id="971a1-136">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="971a1-136">This parameter is not required.</span></span> <span data-ttu-id="971a1-137">Bu parametre sağlanmadıysa cmdlet, veritabanının tehdit algılama ilkesinin bir parçası olarak daha önce tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="971a1-137">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="971a1-138">Bir veritabanı algılama ilkesi ilk kez tanımlandıysa ve bu parametre sağlanmadıysa cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="971a1-138">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="971a1-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="971a1-139">-Confirm</span></span>
<span data-ttu-id="971a1-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="971a1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971a1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971a1-141">-WhatIf</span></span>
<span data-ttu-id="971a1-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="971a1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="971a1-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="971a1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971a1-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971a1-144">-DefaultProfile</span></span>
<span data-ttu-id="971a1-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="971a1-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="971a1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971a1-146">CommonParameters</span></span>
<span data-ttu-id="971a1-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="971a1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971a1-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="971a1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971a1-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="971a1-149">INPUTS</span></span>

###  
<span data-ttu-id="971a1-150">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="971a1-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="971a1-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="971a1-151">OUTPUTS</span></span>

### <span data-ttu-id="971a1-152">Microsoft. Azure. Commands. Sql. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="971a1-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="971a1-153">Bu cmdlet bir **ServerThreatDetectionPolicyModel** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="971a1-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="971a1-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="971a1-154">NOTES</span></span>

## <span data-ttu-id="971a1-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="971a1-155">RELATED LINKS</span></span>

[<span data-ttu-id="971a1-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="971a1-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="971a1-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="971a1-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="971a1-158">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="971a1-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
