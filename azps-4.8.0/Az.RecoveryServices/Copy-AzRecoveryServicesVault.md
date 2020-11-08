---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109386"
---
# <span data-ttu-id="67276-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="67276-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="67276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67276-102">SYNOPSIS</span></span>
<span data-ttu-id="67276-103">Bir bölgedeki kasadaki verileri başka bir bölgedeki kasaya kopyalar.</span><span class="sxs-lookup"><span data-stu-id="67276-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="67276-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67276-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="67276-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67276-105">DESCRIPTION</span></span>
<span data-ttu-id="67276-106">**Copy-Azrecoveryserviceskasa** cmdlet 'i bir bölgedeki kasadaki verileri başka bir bölgedeki kasaya kopyalar.</span><span class="sxs-lookup"><span data-stu-id="67276-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="67276-107">Şu anda yalnızca kasa düzeyinde veri taşımayı destekliyoruz.</span><span class="sxs-lookup"><span data-stu-id="67276-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="67276-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67276-108">EXAMPLES</span></span>

### <span data-ttu-id="67276-109">Örnek 1: vault1 'dan vault2 'a veri kopyalama</span><span class="sxs-lookup"><span data-stu-id="67276-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="67276-110">-Force</span><span class="sxs-lookup"><span data-stu-id="67276-110">-Force</span></span>
<span data-ttu-id="67276-111">Hedef Kasası depolama artıklık türü için onay istemeden, veri taşıma işlemini (onay iletişim kutusunu engeller) zorlar.</span><span class="sxs-lookup"><span data-stu-id="67276-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="67276-112">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="67276-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="67276-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="67276-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="67276-114">Yalnızca kaynak kasasındaki yalnızca henüz taşınamaz olan kapsayıcılar için verileri taşıma</span><span class="sxs-lookup"><span data-stu-id="67276-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="67276-115">-Sourcekasa</span><span class="sxs-lookup"><span data-stu-id="67276-115">-SourceVault</span></span>
<span data-ttu-id="67276-116">Taşınacak kaynak Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67276-116">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67276-117">-Targetkasa</span><span class="sxs-lookup"><span data-stu-id="67276-117">-TargetVault</span></span>
<span data-ttu-id="67276-118">Verilerin taşınacağı hedef kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67276-118">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67276-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67276-119">CommonParameters</span></span>
<span data-ttu-id="67276-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67276-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67276-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="67276-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67276-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67276-122">INPUTS</span></span>

### <span data-ttu-id="67276-123">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="67276-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="67276-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67276-124">OUTPUTS</span></span>

### <span data-ttu-id="67276-125">System. String</span><span class="sxs-lookup"><span data-stu-id="67276-125">System.String</span></span>

## <span data-ttu-id="67276-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67276-126">NOTES</span></span>

## <span data-ttu-id="67276-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67276-127">RELATED LINKS</span></span>
