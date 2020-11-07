---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c76c2ebf40f360820ec3eef719b33142daacdbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759628"
---
# <span data-ttu-id="83b58-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="83b58-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="83b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b58-102">SYNOPSIS</span></span>
<span data-ttu-id="83b58-103">Belirtilen ASR depolama sınıflandırması eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="83b58-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="83b58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83b58-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b58-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83b58-105">DESCRIPTION</span></span>
<span data-ttu-id="83b58-106">**Remove-Azrecoveryservicesasrstorageclassıficationmapping** cmdlet 'ı belirtilen Azure Site Recovery depolama sınıflandırması eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="83b58-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="83b58-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83b58-107">EXAMPLES</span></span>

### <span data-ttu-id="83b58-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="83b58-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="83b58-109">Belirtilen depolama sınıflandırması eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="83b58-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="83b58-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83b58-110">PARAMETERS</span></span>

### <span data-ttu-id="83b58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b58-111">-DefaultProfile</span></span>
<span data-ttu-id="83b58-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83b58-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="83b58-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83b58-113">-InputObject</span></span>
<span data-ttu-id="83b58-114">Cmdlet 'e giriş nesnesi: ASR depolama sınıflandırması eşlemesine, ASR depolama sınıflandırması eşleme nesnesi silinecektir.</span><span class="sxs-lookup"><span data-stu-id="83b58-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="83b58-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="83b58-115">-Confirm</span></span>
<span data-ttu-id="83b58-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83b58-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b58-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b58-117">-WhatIf</span></span>
<span data-ttu-id="83b58-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83b58-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83b58-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83b58-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b58-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b58-120">CommonParameters</span></span>
<span data-ttu-id="83b58-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83b58-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b58-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b58-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b58-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83b58-123">INPUTS</span></span>

### <span data-ttu-id="83b58-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="83b58-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="83b58-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83b58-125">OUTPUTS</span></span>

### <span data-ttu-id="83b58-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="83b58-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="83b58-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83b58-127">NOTES</span></span>

## <span data-ttu-id="83b58-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83b58-128">RELATED LINKS</span></span>

[<span data-ttu-id="83b58-129">Get-Azrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="83b58-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="83b58-130">New-Azrecoveryservicesasrstorageclassıficationmapping</span><span class="sxs-lookup"><span data-stu-id="83b58-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
