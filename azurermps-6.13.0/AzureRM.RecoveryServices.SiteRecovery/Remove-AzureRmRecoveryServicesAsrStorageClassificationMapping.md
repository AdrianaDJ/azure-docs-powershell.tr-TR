---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: bafa671431c617807fa28e2d4fbfed57236fc6a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590077"
---
# <span data-ttu-id="dbda0-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="dbda0-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="dbda0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbda0-102">SYNOPSIS</span></span>
<span data-ttu-id="dbda0-103">Belirtilen ASR depolama sınıflandırması eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="dbda0-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbda0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbda0-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbda0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbda0-105">DESCRIPTION</span></span>
<span data-ttu-id="dbda0-106">**Remove-Azurermrecoveryservicesasrstorageclassıficationmapping** cmdlet 'ı belirtilen Azure Site Recovery depolama sınıflandırması eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="dbda0-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="dbda0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbda0-107">EXAMPLES</span></span>

### <span data-ttu-id="dbda0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dbda0-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="dbda0-109">Belirtilen depolama sınıflandırması eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="dbda0-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="dbda0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbda0-110">PARAMETERS</span></span>

### <span data-ttu-id="dbda0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbda0-111">-DefaultProfile</span></span>
<span data-ttu-id="dbda0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbda0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dbda0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbda0-113">-InputObject</span></span>
<span data-ttu-id="dbda0-114">Cmdlet 'e giriş nesnesi: ASR depolama sınıflandırması eşlemesine, ASR depolama sınıflandırması eşleme nesnesi silinecektir.</span><span class="sxs-lookup"><span data-stu-id="dbda0-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbda0-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbda0-115">-Confirm</span></span>
<span data-ttu-id="dbda0-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbda0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbda0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbda0-117">-WhatIf</span></span>
<span data-ttu-id="dbda0-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbda0-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbda0-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbda0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbda0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbda0-120">CommonParameters</span></span>
<span data-ttu-id="dbda0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbda0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbda0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbda0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbda0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbda0-123">INPUTS</span></span>

### <span data-ttu-id="dbda0-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="dbda0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="dbda0-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbda0-125">OUTPUTS</span></span>

### <span data-ttu-id="dbda0-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dbda0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dbda0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbda0-127">NOTES</span></span>

## <span data-ttu-id="dbda0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbda0-128">RELATED LINKS</span></span>

[<span data-ttu-id="dbda0-129">Get-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="dbda0-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="dbda0-130">New-Azurermrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="dbda0-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
