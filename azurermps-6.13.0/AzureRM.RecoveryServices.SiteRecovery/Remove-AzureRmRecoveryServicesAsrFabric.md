---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8a7b36b67b0ec1721da36dfeba920b556892c5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593660"
---
# <span data-ttu-id="b4fdb-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b4fdb-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="b4fdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fdb-103">Belirtilen Azure Site Recovery yapınızı kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4fdb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4fdb-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4fdb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4fdb-105">DESCRIPTION</span></span>
<span data-ttu-id="b4fdb-106">**Remove-AzureRmRecoveryServicesAsrFabric** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen Azure Site Recovery yapınızı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="b4fdb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4fdb-107">EXAMPLES</span></span>

### <span data-ttu-id="b4fdb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4fdb-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="b4fdb-109">Belirtilen yapının silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b4fdb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4fdb-110">PARAMETERS</span></span>

### <span data-ttu-id="b4fdb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fdb-111">-DefaultProfile</span></span>
<span data-ttu-id="b4fdb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b4fdb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b4fdb-113">-Force</span></span>
<span data-ttu-id="b4fdb-114">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="b4fdb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4fdb-115">-InputObject</span></span>
<span data-ttu-id="b4fdb-116">Cmdlet 'e giriş nesnesi: silinecek yapıya karşılık gelen ASR Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4fdb-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4fdb-117">-Confirm</span></span>
<span data-ttu-id="b4fdb-118">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-118">Specify if confirmation is required.</span></span> <span data-ttu-id="b4fdb-119">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="b4fdb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4fdb-120">-WhatIf</span></span>
<span data-ttu-id="b4fdb-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="b4fdb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fdb-122">CommonParameters</span></span>
<span data-ttu-id="b4fdb-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fdb-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4fdb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fdb-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4fdb-125">INPUTS</span></span>

### <span data-ttu-id="b4fdb-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b4fdb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b4fdb-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4fdb-127">OUTPUTS</span></span>

### <span data-ttu-id="b4fdb-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b4fdb-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b4fdb-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4fdb-129">NOTES</span></span>

## <span data-ttu-id="b4fdb-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4fdb-130">RELATED LINKS</span></span>

[<span data-ttu-id="b4fdb-131">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b4fdb-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="b4fdb-132">Yeni-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="b4fdb-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
