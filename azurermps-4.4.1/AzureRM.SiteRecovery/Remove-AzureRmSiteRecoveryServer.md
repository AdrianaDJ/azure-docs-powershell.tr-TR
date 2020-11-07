---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 4be04d590adbf75760472f4047b7de9efcffd2d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764768"
---
# <span data-ttu-id="ee134-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ee134-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="ee134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee134-102">SYNOPSIS</span></span>
<span data-ttu-id="ee134-103">Geçerli kasadan site kurtarma sunucusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ee134-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee134-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee134-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee134-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee134-105">DESCRIPTION</span></span>
<span data-ttu-id="ee134-106">**Remove-AzureRmSiteRecoveryServer** cmdlet 'i geçerli kasadan kaldıran bir Azure Site kurtarma sunucusu kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="ee134-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="ee134-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee134-107">EXAMPLES</span></span>

## <span data-ttu-id="ee134-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee134-108">PARAMETERS</span></span>

### <span data-ttu-id="ee134-109">-Force</span><span class="sxs-lookup"><span data-stu-id="ee134-109">-Force</span></span>
<span data-ttu-id="ee134-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ee134-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee134-111">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="ee134-111">-Server</span></span>
<span data-ttu-id="ee134-112">Site kurtarma sunucusu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee134-112">Specifies the Site Recovery server object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee134-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee134-113">-Confirm</span></span>
<span data-ttu-id="ee134-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee134-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee134-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee134-115">-WhatIf</span></span>
<span data-ttu-id="ee134-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee134-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ee134-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee134-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee134-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee134-118">-DefaultProfile</span></span>
<span data-ttu-id="ee134-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee134-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee134-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee134-120">CommonParameters</span></span>
<span data-ttu-id="ee134-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee134-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee134-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee134-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee134-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee134-123">INPUTS</span></span>

### <span data-ttu-id="ee134-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="ee134-124">ASRServer</span></span>
<span data-ttu-id="ee134-125">' Server ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="ee134-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="ee134-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee134-126">OUTPUTS</span></span>

### <span data-ttu-id="ee134-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="ee134-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="ee134-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee134-128">NOTES</span></span>

## <span data-ttu-id="ee134-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee134-129">RELATED LINKS</span></span>

[<span data-ttu-id="ee134-130">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ee134-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="ee134-131">Güncelleştirme-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ee134-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)