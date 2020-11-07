---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 2613761db4a975f1bd4e04458ccdc5df81c0a2d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759761"
---
# <span data-ttu-id="8a689-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="8a689-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="8a689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a689-102">SYNOPSIS</span></span>
<span data-ttu-id="8a689-103">Korunabilir öğe için Otomatik yedeklemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8a689-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="8a689-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a689-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a689-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a689-105">DESCRIPTION</span></span>
<span data-ttu-id="8a689-106">**Disable-AzRecoveryServicesBackupAutoProtection** cmdlet 'i korunabilir olan bir öğedeki korumayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8a689-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="8a689-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a689-107">EXAMPLES</span></span>

### <span data-ttu-id="8a689-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8a689-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="8a689-109">İlk cmdlet yedek koruma ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8a689-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="8a689-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a689-110">PARAMETERS</span></span>

### <span data-ttu-id="8a689-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8a689-111">-BackupManagementType</span></span>
<span data-ttu-id="8a689-112">Kaynağın yedekleme yönetimi türü (örneğin: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="8a689-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a689-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a689-113">-DefaultProfile</span></span>
<span data-ttu-id="8a689-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a689-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a689-115">-Inputıtem</span><span class="sxs-lookup"><span data-stu-id="8a689-115">-InputItem</span></span>
<span data-ttu-id="8a689-116">Öğe kimliği</span><span class="sxs-lookup"><span data-stu-id="8a689-116">Item Id</span></span>

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

### <span data-ttu-id="8a689-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8a689-117">-PassThru</span></span>
<span data-ttu-id="8a689-118">Otomatik koruma için sonucu döndürün.</span><span class="sxs-lookup"><span data-stu-id="8a689-118">Return the result for auto protection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a689-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8a689-119">-VaultId</span></span>
<span data-ttu-id="8a689-120">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8a689-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a689-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="8a689-121">-WorkloadType</span></span>
<span data-ttu-id="8a689-122">Kaynağın iş yükü türü (örneğin: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="8a689-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a689-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a689-123">-Confirm</span></span>
<span data-ttu-id="8a689-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a689-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a689-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a689-125">-WhatIf</span></span>
<span data-ttu-id="8a689-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a689-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a689-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a689-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a689-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a689-128">CommonParameters</span></span>
<span data-ttu-id="8a689-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a689-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8a689-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a689-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a689-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a689-131">INPUTS</span></span>

### <span data-ttu-id="8a689-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8a689-132">System.String</span></span>

## <span data-ttu-id="8a689-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a689-133">OUTPUTS</span></span>

### <span data-ttu-id="8a689-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a689-134">System.Boolean</span></span>

## <span data-ttu-id="8a689-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a689-135">NOTES</span></span>

## <span data-ttu-id="8a689-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a689-136">RELATED LINKS</span></span>
