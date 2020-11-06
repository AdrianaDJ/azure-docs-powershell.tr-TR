---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: bb4009edce4e447daacd4cd32835bebc8655dba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589150"
---
# <span data-ttu-id="6ec82-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="6ec82-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="6ec82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec82-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec82-103">Yedekleme yönetiminin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ec82-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ec82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ec82-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ec82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ec82-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec82-106">**Set-AzureRmRecoveryServicesBackupProperties** cmdlet 'ı, kurtarma hizmetleri Kasası için yedekleme depolama özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ec82-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="6ec82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ec82-107">EXAMPLES</span></span>

### <span data-ttu-id="6ec82-108">Örnek 1: kasa için Jeo uzamsal depolama ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ec82-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="6ec82-109">İlk komut Testkasası adlı kasayı alır ve $Vault 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6ec82-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="6ec82-110">İkinci komut $Vault 01 yedek depolama fazlaesini Geoyedekli olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ec82-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="6ec82-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ec82-111">PARAMETERS</span></span>

### <span data-ttu-id="6ec82-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="6ec82-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="6ec82-113">Yedek depolama artıklık türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ec82-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec82-114">-Kasa</span><span class="sxs-lookup"><span data-stu-id="6ec82-114">-Vault</span></span>
<span data-ttu-id="6ec82-115">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ec82-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="6ec82-116">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ec82-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec82-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ec82-117">-Confirm</span></span>
<span data-ttu-id="6ec82-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ec82-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ec82-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ec82-119">-WhatIf</span></span>
<span data-ttu-id="6ec82-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ec82-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ec82-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ec82-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ec82-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec82-122">-DefaultProfile</span></span>
<span data-ttu-id="6ec82-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ec82-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ec82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec82-124">CommonParameters</span></span>
<span data-ttu-id="6ec82-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ec82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec82-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec82-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec82-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ec82-127">INPUTS</span></span>

### <span data-ttu-id="6ec82-128">Arskasa</span><span class="sxs-lookup"><span data-stu-id="6ec82-128">ARSVault</span></span>
<span data-ttu-id="6ec82-129">Parametre ' kasa ', ardışık düzenin ' Arskasa ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6ec82-129">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="6ec82-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ec82-130">OUTPUTS</span></span>

## <span data-ttu-id="6ec82-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ec82-131">NOTES</span></span>

## <span data-ttu-id="6ec82-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ec82-132">RELATED LINKS</span></span>

[<span data-ttu-id="6ec82-133">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="6ec82-133">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="6ec82-134">Get-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="6ec82-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


