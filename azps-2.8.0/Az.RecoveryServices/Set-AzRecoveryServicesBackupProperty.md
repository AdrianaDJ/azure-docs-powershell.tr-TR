---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 6912f54810baeeab795e5f2efca4a51ecafe1c93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933456"
---
# <span data-ttu-id="c9beb-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="c9beb-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="c9beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9beb-102">SYNOPSIS</span></span>
<span data-ttu-id="c9beb-103">Yedekleme yönetiminin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9beb-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="c9beb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9beb-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9beb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9beb-105">DESCRIPTION</span></span>
<span data-ttu-id="c9beb-106">**Set-AzRecoveryServicesBackupProperty** cmdlet 'ı, kurtarma hizmetleri Kasası için yedekleme depolama özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9beb-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="c9beb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9beb-107">EXAMPLES</span></span>

### <span data-ttu-id="c9beb-108">Örnek 1: kasa için Jeo uzamsal depolama ayarlama</span><span class="sxs-lookup"><span data-stu-id="c9beb-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="c9beb-109">İlk komut Testkasası adlı kasayı alır ve $Vault 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c9beb-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="c9beb-110">İkinci komut $Vault 01 yedek depolama fazlaesini Geoyedekli olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9beb-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="c9beb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9beb-111">PARAMETERS</span></span>

### <span data-ttu-id="c9beb-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="c9beb-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="c9beb-113">Yedek depolama artıklık türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9beb-113">Specifies the backup storage redundancy type.</span></span>

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

### <span data-ttu-id="c9beb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9beb-114">-DefaultProfile</span></span>
<span data-ttu-id="c9beb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9beb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9beb-116">-Kasa</span><span class="sxs-lookup"><span data-stu-id="c9beb-116">-Vault</span></span>
<span data-ttu-id="c9beb-117">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9beb-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="c9beb-118">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c9beb-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="c9beb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9beb-119">-Confirm</span></span>
<span data-ttu-id="c9beb-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9beb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9beb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9beb-121">-WhatIf</span></span>
<span data-ttu-id="c9beb-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9beb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9beb-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9beb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9beb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9beb-124">CommonParameters</span></span>
<span data-ttu-id="c9beb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9beb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9beb-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9beb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9beb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9beb-127">INPUTS</span></span>

### <span data-ttu-id="c9beb-128">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="c9beb-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="c9beb-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9beb-129">OUTPUTS</span></span>

### <span data-ttu-id="c9beb-130">System. void</span><span class="sxs-lookup"><span data-stu-id="c9beb-130">System.Void</span></span>

## <span data-ttu-id="c9beb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9beb-131">NOTES</span></span>

## <span data-ttu-id="c9beb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9beb-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9beb-133">Get-Azrecoveryservicesbackupözelliği</span><span class="sxs-lookup"><span data-stu-id="c9beb-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="c9beb-134">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="c9beb-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


