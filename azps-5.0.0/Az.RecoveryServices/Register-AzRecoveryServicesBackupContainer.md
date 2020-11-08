---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278049"
---
# <span data-ttu-id="ddcd5-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ddcd5-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="ddcd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddcd5-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcd5-103">**Register-AzRecoveryServicesBackupContainer** cmdlet 'ı belirli workloadType ile AzureWorkloads Için BIR Azure VM kaydeder.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="ddcd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddcd5-104">SYNTAX</span></span>

### <span data-ttu-id="ddcd5-105">Kaydet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ddcd5-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddcd5-106">Diğiniz</span><span class="sxs-lookup"><span data-stu-id="ddcd5-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddcd5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddcd5-107">DESCRIPTION</span></span>
<span data-ttu-id="ddcd5-108">Bu komut, Azure Backup 'ın kaynağı, söz konusu kurtarma hizmetleri kasasına kaydedilen bir yedek kapsayıcıya dönüştürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="ddcd5-109">Azure yedekleme hizmeti daha sonra bu kapsayıcıdaki belirli iş yükü türünün iş yüklerini daha sonra korunabilir şekilde bulabilir.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="ddcd5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddcd5-110">EXAMPLES</span></span>

### <span data-ttu-id="ddcd5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ddcd5-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="ddcd5-112">Cmdlet, iş yükü MSSQL için kapsayıcı olarak bir Azure VM kaydeder.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="ddcd5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddcd5-113">PARAMETERS</span></span>

### <span data-ttu-id="ddcd5-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ddcd5-114">-BackupManagementType</span></span>
<span data-ttu-id="ddcd5-115">Korunan kaynakların sınıfı.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-115">The class of resources being protected.</span></span> <span data-ttu-id="ddcd5-116">Şu anda bu cmdlet için desteklenen değer AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="ddcd5-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcd5-117">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ddcd5-117">-Container</span></span>
<span data-ttu-id="ddcd5-118">Öğenin bulunduğu kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ddcd5-118">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddcd5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcd5-119">-DefaultProfile</span></span>
<span data-ttu-id="ddcd5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddcd5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ddcd5-121">-Force</span></span>
<span data-ttu-id="ddcd5-122">Kayıt kapsayıcısını zorunlu kılın (onay iletişim kutusu).</span><span class="sxs-lookup"><span data-stu-id="ddcd5-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="ddcd5-123">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="ddcd5-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ddcd5-124">-ResourceId</span></span>
<span data-ttu-id="ddcd5-125">Abonelikteki bazı RecoveryServices Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddcd5-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ddcd5-126">-VaultId</span></span>
<span data-ttu-id="ddcd5-127">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ddcd5-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ddcd5-128">-WorkloadType</span></span>
<span data-ttu-id="ddcd5-129">Kaynağın iş yükü türü.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-129">Workload type of the resource.</span></span> <span data-ttu-id="ddcd5-130">Desteklenen geçerli değer AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="ddcd5-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="ddcd5-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="ddcd5-131">-Confirm</span></span>
<span data-ttu-id="ddcd5-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddcd5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddcd5-133">-WhatIf</span></span>
<span data-ttu-id="ddcd5-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ddcd5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcd5-135">CommonParameters</span></span>
<span data-ttu-id="ddcd5-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcd5-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ddcd5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcd5-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddcd5-138">INPUTS</span></span>

### <span data-ttu-id="ddcd5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ddcd5-139">System.String</span></span>

## <span data-ttu-id="ddcd5-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddcd5-140">OUTPUTS</span></span>

### <span data-ttu-id="ddcd5-141">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="ddcd5-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="ddcd5-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddcd5-142">NOTES</span></span>

## <span data-ttu-id="ddcd5-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddcd5-143">RELATED LINKS</span></span>
