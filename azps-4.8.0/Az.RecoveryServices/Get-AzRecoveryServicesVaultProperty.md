---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265805"
---
# <span data-ttu-id="9e1d7-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="9e1d7-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="9e1d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e1d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1d7-103">Bir kurtarma hizmetleri Kasası özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e1d7-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="9e1d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e1d7-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e1d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e1d7-105">DESCRIPTION</span></span>
<span data-ttu-id="9e1d7-106">**Get-AzRecoveryServicesVaultProperty** cmdlet 'i, bir kurtarma hizmetleri kasasındaki özelliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e1d7-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="9e1d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e1d7-107">EXAMPLES</span></span>

### <span data-ttu-id="9e1d7-108">Örnek 1: kasanın özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="9e1d7-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="9e1d7-109">İlk komut bir kasa nesnesi alır ve $vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e1d7-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="9e1d7-110">İkinci komut kasa özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="9e1d7-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="9e1d7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e1d7-111">PARAMETERS</span></span>

### <span data-ttu-id="9e1d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1d7-112">-DefaultProfile</span></span>
<span data-ttu-id="9e1d7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e1d7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e1d7-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9e1d7-114">-VaultId</span></span>
<span data-ttu-id="9e1d7-115">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9e1d7-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9e1d7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1d7-116">CommonParameters</span></span>
<span data-ttu-id="9e1d7-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e1d7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1d7-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9e1d7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1d7-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e1d7-119">INPUTS</span></span>

### <span data-ttu-id="9e1d7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="9e1d7-120">System.String</span></span>

## <span data-ttu-id="9e1d7-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e1d7-121">OUTPUTS</span></span>

### <span data-ttu-id="9e1d7-122">Microsoft. Azure. Management. RecoveryServices. Backup. modeller. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="9e1d7-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="9e1d7-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e1d7-123">NOTES</span></span>

## <span data-ttu-id="9e1d7-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e1d7-124">RELATED LINKS</span></span>

[<span data-ttu-id="9e1d7-125">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="9e1d7-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="9e1d7-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="9e1d7-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
