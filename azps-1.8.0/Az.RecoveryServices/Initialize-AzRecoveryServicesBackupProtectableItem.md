---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 0fd0473cccdf8fbef3d3bab941ab6b3ce7813a63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759677"
---
# <span data-ttu-id="58212-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="58212-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="58212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58212-102">SYNOPSIS</span></span>
<span data-ttu-id="58212-103">Bu komut, verilen kapsayıcıda verilen iş yükü türündeki korumasız öğelerin herhangi birinin bulunmasını tetikler.</span><span class="sxs-lookup"><span data-stu-id="58212-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="58212-104">DB uygulaması otomatik olarak korunmuyorsa, bu komutu eklendiğinde yeni DBs 'yi keşfetmek ve korumak için bu komutu kullanın.</span><span class="sxs-lookup"><span data-stu-id="58212-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="58212-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58212-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58212-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="58212-106">DESCRIPTION</span></span>
<span data-ttu-id="58212-107">bir kapsayıcıdaki belirli iş yükleri için cmdlet 'i arar.</span><span class="sxs-lookup"><span data-stu-id="58212-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="58212-108">Bu işlem, korunabilir öğeler oluşturan bir işlemi tetikler.</span><span class="sxs-lookup"><span data-stu-id="58212-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="58212-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58212-109">EXAMPLES</span></span>

### <span data-ttu-id="58212-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="58212-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container –WorkloadType “MSSQL”
```

<span data-ttu-id="58212-111">Cmdlet, yeni korunabilir öğeler için bir keşif işlemi yürütür.</span><span class="sxs-lookup"><span data-stu-id="58212-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="58212-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58212-112">PARAMETERS</span></span>

### <span data-ttu-id="58212-113">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="58212-113">-Container</span></span>
<span data-ttu-id="58212-114">Öğenin bulunduğu kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="58212-114">Container where the item resides</span></span>

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

### <span data-ttu-id="58212-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58212-115">-DefaultProfile</span></span>
<span data-ttu-id="58212-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58212-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58212-117">-VaultId</span><span class="sxs-lookup"><span data-stu-id="58212-117">-VaultId</span></span>
<span data-ttu-id="58212-118">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="58212-118">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="58212-119">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="58212-119">-WorkloadType</span></span>
<span data-ttu-id="58212-120">Kaynağın iş yükü türü (örneğin: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="58212-120">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="58212-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58212-121">CommonParameters</span></span>
<span data-ttu-id="58212-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58212-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58212-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58212-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58212-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58212-124">INPUTS</span></span>

### <span data-ttu-id="58212-125">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="58212-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="58212-126">System. String</span><span class="sxs-lookup"><span data-stu-id="58212-126">System.String</span></span>

## <span data-ttu-id="58212-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58212-127">OUTPUTS</span></span>

### <span data-ttu-id="58212-128">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="58212-128">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="58212-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58212-129">NOTES</span></span>

## <span data-ttu-id="58212-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58212-130">RELATED LINKS</span></span>