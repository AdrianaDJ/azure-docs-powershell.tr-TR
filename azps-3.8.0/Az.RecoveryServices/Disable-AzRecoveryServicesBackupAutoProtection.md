---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 97eae8c5c545297a7d6287a951ec02433d591168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938287"
---
# <span data-ttu-id="e5291-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="e5291-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="e5291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5291-102">SYNOPSIS</span></span>
<span data-ttu-id="e5291-103">Korunabilir öğe için Otomatik yedeklemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e5291-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="e5291-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5291-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5291-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5291-105">DESCRIPTION</span></span>
<span data-ttu-id="e5291-106">**Disable-AzRecoveryServicesBackupAutoProtection** cmdlet 'i korunabilir olan bir öğedeki korumayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e5291-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="e5291-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5291-107">EXAMPLES</span></span>

### <span data-ttu-id="e5291-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5291-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="e5291-109">İlk cmdlet yedek koruma ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e5291-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="e5291-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5291-110">PARAMETERS</span></span>

### <span data-ttu-id="e5291-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e5291-111">-BackupManagementType</span></span>
<span data-ttu-id="e5291-112">Kaynağın yedekleme yönetimi türü (örneğin: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="e5291-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

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

### <span data-ttu-id="e5291-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5291-113">-DefaultProfile</span></span>
<span data-ttu-id="e5291-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5291-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5291-115">-Inputıtem</span><span class="sxs-lookup"><span data-stu-id="e5291-115">-InputItem</span></span>
<span data-ttu-id="e5291-116">Öğe kimliği</span><span class="sxs-lookup"><span data-stu-id="e5291-116">Item Id</span></span>

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

### <span data-ttu-id="e5291-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e5291-117">-PassThru</span></span>
<span data-ttu-id="e5291-118">Otomatik koruma için sonucu döndürün.</span><span class="sxs-lookup"><span data-stu-id="e5291-118">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="e5291-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e5291-119">-VaultId</span></span>
<span data-ttu-id="e5291-120">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e5291-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e5291-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e5291-121">-WorkloadType</span></span>
<span data-ttu-id="e5291-122">Kaynağın iş yükü türü (örneğin: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="e5291-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

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

### <span data-ttu-id="e5291-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5291-123">-Confirm</span></span>
<span data-ttu-id="e5291-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5291-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5291-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5291-125">-WhatIf</span></span>
<span data-ttu-id="e5291-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5291-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5291-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5291-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5291-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5291-128">CommonParameters</span></span>
<span data-ttu-id="e5291-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5291-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5291-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e5291-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5291-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5291-131">INPUTS</span></span>

### <span data-ttu-id="e5291-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e5291-132">System.String</span></span>

## <span data-ttu-id="e5291-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5291-133">OUTPUTS</span></span>

### <span data-ttu-id="e5291-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5291-134">System.Boolean</span></span>

## <span data-ttu-id="e5291-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5291-135">NOTES</span></span>

## <span data-ttu-id="e5291-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5291-136">RELATED LINKS</span></span>
