---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104708"
---
# <span data-ttu-id="e608c-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e608c-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="e608c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e608c-102">SYNOPSIS</span></span>
<span data-ttu-id="e608c-103">Bu komut, verilen kapsayıcıda verilen iş yükü türündeki korumasız öğelerin herhangi birinin bulunmasını tetikler.</span><span class="sxs-lookup"><span data-stu-id="e608c-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="e608c-104">DB uygulaması otomatik olarak korunmuyorsa, bu komutu eklendiğinde yeni DBs 'yi keşfetmek ve korumak için bu komutu kullanın.</span><span class="sxs-lookup"><span data-stu-id="e608c-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="e608c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e608c-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e608c-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="e608c-106">DESCRIPTION</span></span>
<span data-ttu-id="e608c-107">bir kapsayıcıdaki belirli iş yükleri için cmdlet 'i arar.</span><span class="sxs-lookup"><span data-stu-id="e608c-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="e608c-108">Bu işlem, korunabilir öğeler oluşturan bir işlemi tetikler.</span><span class="sxs-lookup"><span data-stu-id="e608c-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="e608c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e608c-109">EXAMPLES</span></span>

### <span data-ttu-id="e608c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e608c-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="e608c-111">Cmdlet, yeni korunabilir öğeler için bir keşif işlemi yürütür.</span><span class="sxs-lookup"><span data-stu-id="e608c-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="e608c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e608c-112">PARAMETERS</span></span>

### <span data-ttu-id="e608c-113">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="e608c-113">-Container</span></span>
<span data-ttu-id="e608c-114">Öğenin bulunduğu kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="e608c-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e608c-115">-DefaultProfile</span></span>
<span data-ttu-id="e608c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e608c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e608c-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e608c-117">-PassThru</span></span>
<span data-ttu-id="e608c-118">Silinecek kapsayıcıyı döndürün.</span><span class="sxs-lookup"><span data-stu-id="e608c-118">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="e608c-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e608c-119">-VaultId</span></span>
<span data-ttu-id="e608c-120">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e608c-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e608c-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e608c-121">-WorkloadType</span></span>
<span data-ttu-id="e608c-122">Kaynağın iş yükü türü (örneğin: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="e608c-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e608c-123">-Confirm</span></span>
<span data-ttu-id="e608c-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e608c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e608c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e608c-125">-WhatIf</span></span>
<span data-ttu-id="e608c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e608c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e608c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e608c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e608c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e608c-128">CommonParameters</span></span>
<span data-ttu-id="e608c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e608c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e608c-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e608c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e608c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e608c-131">INPUTS</span></span>

### <span data-ttu-id="e608c-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e608c-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="e608c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e608c-133">System.String</span></span>

## <span data-ttu-id="e608c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e608c-134">OUTPUTS</span></span>

### <span data-ttu-id="e608c-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="e608c-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="e608c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e608c-136">NOTES</span></span>

## <span data-ttu-id="e608c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e608c-137">RELATED LINKS</span></span>
