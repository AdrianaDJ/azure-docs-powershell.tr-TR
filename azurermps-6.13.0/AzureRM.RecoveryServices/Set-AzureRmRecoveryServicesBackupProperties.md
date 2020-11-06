---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: 7fa55bd306a1cbe04ddf3af63a66682a0fa17f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587192"
---
# <span data-ttu-id="8cd34-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="8cd34-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="8cd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cd34-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd34-103">Yedekleme yönetiminin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8cd34-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cd34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8cd34-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cd34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8cd34-105">DESCRIPTION</span></span>
<span data-ttu-id="8cd34-106">**Set-AzureRmRecoveryServicesBackupProperties** cmdlet 'ı, kurtarma hizmetleri Kasası için yedekleme depolama özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8cd34-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="8cd34-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8cd34-107">EXAMPLES</span></span>

### <span data-ttu-id="8cd34-108">Örnek 1: kasa için Jeo uzamsal depolama ayarlama</span><span class="sxs-lookup"><span data-stu-id="8cd34-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="8cd34-109">İlk komut Testkasası adlı kasayı alır ve $Vault 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8cd34-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="8cd34-110">İkinci komut $Vault 01 yedek depolama fazlaesini Geoyedekli olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8cd34-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="8cd34-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8cd34-111">PARAMETERS</span></span>

### <span data-ttu-id="8cd34-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="8cd34-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="8cd34-113">Yedek depolama artıklık türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8cd34-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd34-114">-Kasa</span><span class="sxs-lookup"><span data-stu-id="8cd34-114">-Vault</span></span>
<span data-ttu-id="8cd34-115">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8cd34-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="8cd34-116">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8cd34-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cd34-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="8cd34-117">-Confirm</span></span>
<span data-ttu-id="8cd34-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8cd34-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cd34-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cd34-119">-WhatIf</span></span>
<span data-ttu-id="8cd34-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8cd34-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cd34-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8cd34-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cd34-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd34-122">-DefaultProfile</span></span>
<span data-ttu-id="8cd34-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8cd34-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd34-124">CommonParameters</span></span>
<span data-ttu-id="8cd34-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8cd34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd34-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cd34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd34-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8cd34-127">INPUTS</span></span>

### <span data-ttu-id="8cd34-128">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="8cd34-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="8cd34-129">Parametreler: kasa (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8cd34-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="8cd34-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8cd34-130">OUTPUTS</span></span>

### <span data-ttu-id="8cd34-131">System. void</span><span class="sxs-lookup"><span data-stu-id="8cd34-131">System.Void</span></span>

## <span data-ttu-id="8cd34-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8cd34-132">NOTES</span></span>

## <span data-ttu-id="8cd34-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8cd34-133">RELATED LINKS</span></span>

[<span data-ttu-id="8cd34-134">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="8cd34-134">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="8cd34-135">Get-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="8cd34-135">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


