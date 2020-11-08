---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitorProviderInstance.md
ms.openlocfilehash: f0d8486bc26043ee4f2cb2126c7ffdc64829a7cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109055"
---
# <span data-ttu-id="3e1cd-101">New-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="3e1cd-101">New-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="3e1cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1cd-103">Belirtilen abonelik, kaynak grubu, Sapmonitörünüz adı ve kaynak adı için bir sağlayıcı örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-103">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="3e1cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e1cd-104">SYNTAX</span></span>

### <span data-ttu-id="3e1cd-105">Dize (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e1cd-105">ByString (Default)</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePassword <SecureString> -HanaDatabaseSqlPort <Int32>
 -HanaDatabaseUsername <String> -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>]
 [-Metadata <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3e1cd-106">Bykeykasası</span><span class="sxs-lookup"><span data-stu-id="3e1cd-106">ByKeyVault</span></span>
```
New-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 -HanaDatabaseName <String> -HanaDatabasePasswordKeyVaultResourceId <String>
 -HanaDatabasePasswordSecretId <String> -HanaDatabaseSqlPort <Int32> -HanaDatabaseUsername <String>
 -HanaHostname <String> -ProviderType <String> [-SubscriptionId <String>] [-Metadata <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e1cd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e1cd-107">DESCRIPTION</span></span>
<span data-ttu-id="3e1cd-108">Belirtilen abonelik, kaynak grubu, Sapmonitörünüz adı ve kaynak adı için bir sağlayıcı örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-108">Creates a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="3e1cd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e1cd-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1cd-110">Örnek 1: HANA için dize ile SAP izleme örneği oluşturma</span><span class="sxs-lookup"><span data-stu-id="3e1cd-110">Example 1: Create an instance of SAP monitor by string for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -Name ps-sapmonitorins-t01 -SapMonitorName yemingmonitor -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePassword (ConvertTo-SecureString "Manager1" -AsPlainText -Force)

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="3e1cd-111">Bu komut, HANA için dize kullanarak SAP izlemesi örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-111">This command creates an instance of SAP monitor by string for HANA.</span></span>

### <span data-ttu-id="3e1cd-112">Örnek 2: HANA için Anahtar Kasası tarafından SAP izlemesi örneği oluşturma</span><span class="sxs-lookup"><span data-stu-id="3e1cd-112">Example 2: Create an instance of SAP monitor by key vault for HANA</span></span>
```powershell
PS C:\> New-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName sapMonitor-vayh7q-test -ProviderType SapHana -HanaHostname 'hdb1-0' -HanaDatabaseName 'SYSTEMDB' -HanaDatabaseSqlPort 30015 -HanaDatabaseUsername SYSTEM -HanaDatabasePasswordSecretId https://kv-9gosjc-test.vault.azure.net/secrets/hanaPassword/bf516d1dfcc144138e5cf55114f3344b -HanaDatabasePasswordKeyVaultResourceId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/costmanagement-rg-8p50xe/providers/Microsoft.KeyVault/vaults/kv-9gosjc-test -Name sapins-kv-test

Name           Type
----           ----
sapins-kv-test Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="3e1cd-113">Bu komut, HANA için Anahtar Kasası tarafından SAP izlemesi örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-113">This command creates an instance of SAP monitor by key vault for HANA.</span></span>

## <span data-ttu-id="3e1cd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e1cd-114">PARAMETERS</span></span>

### <span data-ttu-id="3e1cd-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="3e1cd-115">-AsJob</span></span>
<span data-ttu-id="3e1cd-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="3e1cd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3e1cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1cd-117">-DefaultProfile</span></span>
<span data-ttu-id="3e1cd-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-119">-HanaDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e1cd-119">-HanaDatabaseName</span></span>
<span data-ttu-id="3e1cd-120">SAP HANA örneğinin veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-120">The database name of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-121">-HanaDatabasePassword</span><span class="sxs-lookup"><span data-stu-id="3e1cd-121">-HanaDatabasePassword</span></span>
<span data-ttu-id="3e1cd-122">SAP HANA örneğinin veritabanı parolası.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-122">The password of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByString
Aliases: HanaDbPassword

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-123">-Hanadatabasepasswordkeyvaultresourceıd</span><span class="sxs-lookup"><span data-stu-id="3e1cd-123">-HanaDatabasePasswordKeyVaultResourceId</span></span>
<span data-ttu-id="3e1cd-124">HANA kimlik bilgilerini içeren Anahtar Kasası kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-124">Resource ID of the Key Vault that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordKeyVaultId, KeyVaultId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-125">-HanaDatabasePasswordSecretId</span><span class="sxs-lookup"><span data-stu-id="3e1cd-125">-HanaDatabasePasswordSecretId</span></span>
<span data-ttu-id="3e1cd-126">HANA kimlik bilgilerini içeren Anahtar Kasası gizliliğine gizli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-126">Secret identifier to the Key Vault secret that contains the HANA credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyVault
Aliases: HanaDbPasswordSecretId, SecretId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-127">-HanaDatabaseSqlPort</span><span class="sxs-lookup"><span data-stu-id="3e1cd-127">-HanaDatabaseSqlPort</span></span>
<span data-ttu-id="3e1cd-128">SAP HANA örneğinin veritabanı SQL bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-128">The SQL port of the database of SAP HANA instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: HanaDbSqlPort

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-129">-Hanadatabasekullanıcıadı</span><span class="sxs-lookup"><span data-stu-id="3e1cd-129">-HanaDatabaseUsername</span></span>
<span data-ttu-id="3e1cd-130">SAP HANA örneğinin Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-130">The username of the database of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HanaDbUsername

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-131">-Hanaanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="3e1cd-131">-HanaHostname</span></span>
<span data-ttu-id="3e1cd-132">SAP HANA örneğinin ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-132">The hostname of SAP HANA instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3e1cd-133">-Metadata</span></span>
<span data-ttu-id="3e1cd-134">Sağlayıcı örneğinin meta verilerini içeren bir JSON dizesi.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-134">A JSON string containing metadata of the provider instance.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e1cd-135">-Name</span></span>
<span data-ttu-id="3e1cd-136">Sağlayıcı örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-136">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3e1cd-137">-NoWait</span></span>
<span data-ttu-id="3e1cd-138">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="3e1cd-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3e1cd-139">-ProviderType</span><span class="sxs-lookup"><span data-stu-id="3e1cd-139">-ProviderType</span></span>
<span data-ttu-id="3e1cd-140">Sağlayıcı örneğinin türü.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-140">The type of provider instance.</span></span>
<span data-ttu-id="3e1cd-141">Desteklenen değerler: "SapHana".</span><span class="sxs-lookup"><span data-stu-id="3e1cd-141">Supported values are: "SapHana".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1cd-142">-ResourceGroupName</span></span>
<span data-ttu-id="3e1cd-143">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-143">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-144">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="3e1cd-144">-SapMonitorName</span></span>
<span data-ttu-id="3e1cd-145">SAP izleyici kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-145">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-146">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3e1cd-146">-SubscriptionId</span></span>
<span data-ttu-id="3e1cd-147">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-147">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e1cd-148">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1cd-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e1cd-149">-Confirm</span></span>
<span data-ttu-id="3e1cd-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1cd-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1cd-151">-WhatIf</span></span>
<span data-ttu-id="3e1cd-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1cd-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1cd-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1cd-154">CommonParameters</span></span>
<span data-ttu-id="3e1cd-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1cd-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3e1cd-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1cd-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e1cd-157">INPUTS</span></span>

## <span data-ttu-id="3e1cd-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e1cd-158">OUTPUTS</span></span>

### <span data-ttu-id="3e1cd-159">Microsoft. Azure. PowerShell. cmdlet. Hana</span><span class="sxs-lookup"><span data-stu-id="3e1cd-159">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="3e1cd-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e1cd-160">NOTES</span></span>

<span data-ttu-id="3e1cd-161">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="3e1cd-161">ALIASES</span></span>

## <span data-ttu-id="3e1cd-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e1cd-162">RELATED LINKS</span></span>

