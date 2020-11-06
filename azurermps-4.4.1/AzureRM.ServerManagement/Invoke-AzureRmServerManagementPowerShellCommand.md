---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: 5acd510118f2be26ba09f3e0fefbc9b0c80aae02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590643"
---
# <span data-ttu-id="94b86-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="94b86-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="94b86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94b86-102">SYNOPSIS</span></span>
<span data-ttu-id="94b86-103">Bir düğümde Windows PowerShell betik bloğunu yürütür.</span><span class="sxs-lookup"><span data-stu-id="94b86-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94b86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94b86-104">SYNTAX</span></span>

### <span data-ttu-id="94b86-105">ByName</span><span class="sxs-lookup"><span data-stu-id="94b86-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b86-106">BySession</span><span class="sxs-lookup"><span data-stu-id="94b86-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94b86-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="94b86-107">DESCRIPTION</span></span>
<span data-ttu-id="94b86-108">**Invoke-AzureRmServerManagementPowerShellCommand** cmdlet 'i, bir Azure Server yönetim ağ geçidiyle yönetilen bir düğümde Windows PowerShell betik bloğunu yürütür.</span><span class="sxs-lookup"><span data-stu-id="94b86-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="94b86-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94b86-109">EXAMPLES</span></span>

## <span data-ttu-id="94b86-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94b86-110">PARAMETERS</span></span>

### <span data-ttu-id="94b86-111">-Komut</span><span class="sxs-lookup"><span data-stu-id="94b86-111">-Command</span></span>
<span data-ttu-id="94b86-112">Hedef düğümde çalıştırılacak komut dosyası bloğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="94b86-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: System.Management.Automation.ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-113">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="94b86-113">-NodeName</span></span>
<span data-ttu-id="94b86-114">Betik bloğunun çalıştırılacağı düğümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94b86-114">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-115">-Powershelloturumadı</span><span class="sxs-lookup"><span data-stu-id="94b86-115">-PowerShellSessionName</span></span>
<span data-ttu-id="94b86-116">Hedef düğümdeki Windows PowerShell çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94b86-116">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-117">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="94b86-117">-RawOutput</span></span>
<span data-ttu-id="94b86-118">Cmdlet 'in, düğümdeki çıktıyı içeren tam nesneyi geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94b86-118">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

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

### <span data-ttu-id="94b86-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b86-119">-ResourceGroupName</span></span>
<span data-ttu-id="94b86-120">Düğümün ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94b86-120">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-121">-Oturum</span><span class="sxs-lookup"><span data-stu-id="94b86-121">-Session</span></span>
<span data-ttu-id="94b86-122">Hedef düğüme bağlanmak için bu cmdlet 'in kullandığı **oturum** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94b86-122">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="94b86-123">Bu parametre, *Resourcegroupname* , *DüğümAdı* , *oturumadı* ve *powershelloturumadı* parametreleri yerine belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="94b86-123">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-124">-OturumAdı</span><span class="sxs-lookup"><span data-stu-id="94b86-124">-SessionName</span></span>
<span data-ttu-id="94b86-125">Düğümü yönetmek için oturumun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94b86-125">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b86-126">-DefaultProfile</span></span>
<span data-ttu-id="94b86-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94b86-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94b86-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b86-128">CommonParameters</span></span>
<span data-ttu-id="94b86-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94b86-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b86-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b86-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b86-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94b86-131">INPUTS</span></span>

### <span data-ttu-id="94b86-132">Oturumu</span><span class="sxs-lookup"><span data-stu-id="94b86-132">Session</span></span>
<span data-ttu-id="94b86-133">Parametre ' Session ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="94b86-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="94b86-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94b86-134">OUTPUTS</span></span>

### <span data-ttu-id="94b86-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="94b86-135">System.Object</span></span>

## <span data-ttu-id="94b86-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94b86-136">NOTES</span></span>

## <span data-ttu-id="94b86-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94b86-137">RELATED LINKS</span></span>

[<span data-ttu-id="94b86-138">Azure Server Yönetim cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="94b86-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


