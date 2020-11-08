---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 6dfff295981ab341d05790e18ed6e4d5c5b0e822
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938217"
---
# <span data-ttu-id="34ba0-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="34ba0-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="34ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="34ba0-103">Bu komut, kullanıcıların var olan korumasız tüm korunmasız değişiklikleri ve söz konusu ilkeyle birlikte eklenecek tüm VERITABANıNı otomatik olarak korumalarına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="34ba0-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="34ba0-104">Böylece, Azure yedekleme hizmeti tüm yeni DBMS 'ler için otomatik olarak korumalı kapsayıcıları tarar ve bunları otomatik olarak korur.</span><span class="sxs-lookup"><span data-stu-id="34ba0-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="34ba0-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34ba0-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34ba0-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="34ba0-106">DESCRIPTION</span></span>
<span data-ttu-id="34ba0-107">**Enable-AzRecoveryServicesBackupAutoProtection** cmdlet 'i korunabilir bir tabloda Azure otomatik yedekleme koruma ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34ba0-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="34ba0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34ba0-108">EXAMPLES</span></span>

### <span data-ttu-id="34ba0-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34ba0-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="34ba0-110">İlk cmdlet varsayılan ilke nesnesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="34ba0-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="34ba0-111">İkinci cmdlet $Pol ilkeyi kullanarak AzureWorkload için yedekleme koruması ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34ba0-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="34ba0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34ba0-112">PARAMETERS</span></span>

### <span data-ttu-id="34ba0-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="34ba0-113">-BackupManagementType</span></span>
<span data-ttu-id="34ba0-114">Kaynağın yedekleme yönetimi türü (örneğin: MAB, DPM, AzureWorkload).</span><span class="sxs-lookup"><span data-stu-id="34ba0-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

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

### <span data-ttu-id="34ba0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ba0-115">-DefaultProfile</span></span>
<span data-ttu-id="34ba0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34ba0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ba0-117">-Inputıtem</span><span class="sxs-lookup"><span data-stu-id="34ba0-117">-InputItem</span></span>
<span data-ttu-id="34ba0-118">Giriş olarak geçirilebilecek korunabilir öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34ba0-118">Specifies the protectable item object that can be passed as an input.</span></span>

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

### <span data-ttu-id="34ba0-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34ba0-119">-PassThru</span></span>
<span data-ttu-id="34ba0-120">Otomatik koruma için sonucu döndürün.</span><span class="sxs-lookup"><span data-stu-id="34ba0-120">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="34ba0-121">-İlke</span><span class="sxs-lookup"><span data-stu-id="34ba0-121">-Policy</span></span>
<span data-ttu-id="34ba0-122">Koruma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="34ba0-122">Protection policy object.</span></span>

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

### <span data-ttu-id="34ba0-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="34ba0-123">-VaultId</span></span>
<span data-ttu-id="34ba0-124">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="34ba0-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="34ba0-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="34ba0-125">-WorkloadType</span></span>
<span data-ttu-id="34ba0-126">Kaynağın iş yükü türü (örneğin: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="34ba0-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="34ba0-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="34ba0-127">-Confirm</span></span>
<span data-ttu-id="34ba0-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34ba0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ba0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ba0-129">-WhatIf</span></span>
<span data-ttu-id="34ba0-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34ba0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34ba0-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34ba0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ba0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ba0-132">CommonParameters</span></span>
<span data-ttu-id="34ba0-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34ba0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ba0-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34ba0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ba0-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34ba0-135">INPUTS</span></span>

### <span data-ttu-id="34ba0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="34ba0-136">System.String</span></span>

## <span data-ttu-id="34ba0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34ba0-137">OUTPUTS</span></span>

### <span data-ttu-id="34ba0-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="34ba0-138">System.Object</span></span>

## <span data-ttu-id="34ba0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34ba0-139">NOTES</span></span>

## <span data-ttu-id="34ba0-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34ba0-140">RELATED LINKS</span></span>