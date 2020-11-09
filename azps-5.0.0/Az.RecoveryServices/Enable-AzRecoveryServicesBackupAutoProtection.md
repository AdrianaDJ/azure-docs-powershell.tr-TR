---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323083"
---
# <span data-ttu-id="d3b2d-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="d3b2d-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="d3b2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b2d-103">**Enable-AzRecoveryServicesBackupAutoProtection** cmdlet 'i, sağlanan ilkeyle verilen örnek içinde güncel ve GELECEKTEKI tüm SQL DBS kopyalarını otomatik olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="d3b2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3b2d-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3b2d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="d3b2d-106">Bu komut, kullanıcıların var olan korumasız SQL DBs ve tüm DB 'leri belirtilen ilkeyle otomatik olarak korumasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="d3b2d-107">Yönerge gelecekteki tüm DBMS 'Leri yedeklemeniz gerektiğinden, işlem bir SQLInstance düzeyinde yapılır, Azure yedekleme hizmeti her yeni DBs için otomatik olarak otomatik korumalı kapsayıcıları tarar ve bunları otomatik olarak korur.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="d3b2d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3b2d-108">EXAMPLES</span></span>

### <span data-ttu-id="d3b2d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3b2d-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="d3b2d-110">İlk cmdlet varsayılan ilke nesnesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="d3b2d-111">İkinci cmdlet, korunabilir bir öğe olan ilgili SQLInstance 'ı getirir.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="d3b2d-112">3. Command daha sonra $Pol ilkeyi kullanarak bu örnek için otomatik korumayı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="d3b2d-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d3b2d-113">Example 2</span></span>

<span data-ttu-id="d3b2d-114">Bu komut, kullanıcıların var olan korumasız tüm korunmasız değişiklikleri ve söz konusu ilkeyle birlikte eklenecek tüm VERITABANıNı otomatik olarak korumalarına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="d3b2d-115">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="d3b2d-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="d3b2d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3b2d-116">PARAMETERS</span></span>

### <span data-ttu-id="d3b2d-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d3b2d-117">-BackupManagementType</span></span>
<span data-ttu-id="d3b2d-118">Korunan kaynakların sınıfı.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-118">The class of resources being protected.</span></span> <span data-ttu-id="d3b2d-119">Şu anda bu cmdlet için desteklenen değerler MAB, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="d3b2d-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b2d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b2d-120">-DefaultProfile</span></span>
<span data-ttu-id="d3b2d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3b2d-122">-Inputıtem</span><span class="sxs-lookup"><span data-stu-id="d3b2d-122">-InputItem</span></span>
<span data-ttu-id="d3b2d-123">Giriş olarak geçirilebilecek korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="d3b2d-124">Desteklenen geçerli değer, "SQLInstance" türünde bir korunabilir öğe nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b2d-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d3b2d-125">-PassThru</span></span>
<span data-ttu-id="d3b2d-126">Otomatik koruma için sonucu döndürün.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="d3b2d-127">-İlke</span><span class="sxs-lookup"><span data-stu-id="d3b2d-127">-Policy</span></span>
<span data-ttu-id="d3b2d-128">Koruma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-128">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b2d-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d3b2d-129">-VaultId</span></span>
<span data-ttu-id="d3b2d-130">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-130">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b2d-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d3b2d-131">-WorkloadType</span></span>
<span data-ttu-id="d3b2d-132">Kaynağın iş yükü türü.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-132">Workload type of the resource.</span></span> <span data-ttu-id="d3b2d-133">Desteklenen geçerli değerler AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="d3b2d-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b2d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3b2d-134">-Confirm</span></span>
<span data-ttu-id="d3b2d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b2d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b2d-136">-WhatIf</span></span>
<span data-ttu-id="d3b2d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="d3b2d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b2d-138">CommonParameters</span></span>
<span data-ttu-id="d3b2d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b2d-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d3b2d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b2d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3b2d-141">INPUTS</span></span>

### <span data-ttu-id="d3b2d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d3b2d-142">System.String</span></span>

## <span data-ttu-id="d3b2d-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3b2d-143">OUTPUTS</span></span>

### <span data-ttu-id="d3b2d-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="d3b2d-144">System.Object</span></span>

## <span data-ttu-id="d3b2d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3b2d-145">NOTES</span></span>

## <span data-ttu-id="d3b2d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3b2d-146">RELATED LINKS</span></span>
