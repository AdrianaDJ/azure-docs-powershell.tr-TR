---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763815"
---
# <span data-ttu-id="87a50-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="87a50-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="87a50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a50-102">SYNOPSIS</span></span>
<span data-ttu-id="87a50-103">ARM kaynağınızın yedeklenip yedeklenmediğini denetler.</span><span class="sxs-lookup"><span data-stu-id="87a50-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87a50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87a50-104">SYNTAX</span></span>

### <span data-ttu-id="87a50-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="87a50-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87a50-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="87a50-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87a50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="87a50-107">DESCRIPTION</span></span>
<span data-ttu-id="87a50-108">Belirtilen kaynak, abonelikteki herhangi bir kurtarma hizmetleri Kasası altında korunmuyorsa komut null/boş döndürür.</span><span class="sxs-lookup"><span data-stu-id="87a50-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="87a50-109">Korunmuşsa, ilgili kasa ayrıntıları geri döndürülecek.</span><span class="sxs-lookup"><span data-stu-id="87a50-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="87a50-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87a50-110">EXAMPLES</span></span>

### <span data-ttu-id="87a50-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="87a50-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="87a50-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87a50-112">PARAMETERS</span></span>

### <span data-ttu-id="87a50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a50-113">-DefaultProfile</span></span>
<span data-ttu-id="87a50-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87a50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a50-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="87a50-115">-Name</span></span>
<span data-ttu-id="87a50-116">Aboneliğindeki bazı kurtarma hizmetleri Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="87a50-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a50-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a50-117">-ResourceGroupName</span></span>
<span data-ttu-id="87a50-118">Aboneliğindeki bazı RecoveryServices Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="87a50-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a50-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="87a50-119">-ResourceId</span></span>
<span data-ttu-id="87a50-120">Abonelikteki bazı RecoveryServices Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="87a50-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a50-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="87a50-121">-Type</span></span>
<span data-ttu-id="87a50-122">Aboneliğindeki bazı kurtarma hizmetleri Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="87a50-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a50-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a50-123">CommonParameters</span></span>
<span data-ttu-id="87a50-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87a50-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a50-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a50-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a50-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87a50-126">INPUTS</span></span>

### <span data-ttu-id="87a50-127">System. String</span><span class="sxs-lookup"><span data-stu-id="87a50-127">System.String</span></span>

## <span data-ttu-id="87a50-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87a50-128">OUTPUTS</span></span>

### <span data-ttu-id="87a50-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="87a50-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="87a50-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87a50-130">NOTES</span></span>

## <span data-ttu-id="87a50-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87a50-131">RELATED LINKS</span></span>
