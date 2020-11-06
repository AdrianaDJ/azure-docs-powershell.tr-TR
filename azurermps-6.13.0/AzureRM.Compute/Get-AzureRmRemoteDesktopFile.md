---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: e6f3ba75247d8b5358e2a97c8bc635bbf805baec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588557"
---
# <span data-ttu-id="8ebda-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="8ebda-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="8ebda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ebda-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebda-103">Bir. rdp dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="8ebda-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ebda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ebda-104">SYNTAX</span></span>

### <span data-ttu-id="8ebda-105">İndirin</span><span class="sxs-lookup"><span data-stu-id="8ebda-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ebda-106">Başlatılması</span><span class="sxs-lookup"><span data-stu-id="8ebda-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ebda-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ebda-107">DESCRIPTION</span></span>
<span data-ttu-id="8ebda-108">**Get-AzureRmRemoteDesktopFile** cmdlet 'ı bir Uzak Masaüstü Protokolü (. rdp) dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="8ebda-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="8ebda-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ebda-109">EXAMPLES</span></span>

### <span data-ttu-id="8ebda-110">Örnek 1: uzak masaüstü dosyası alma</span><span class="sxs-lookup"><span data-stu-id="8ebda-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="8ebda-111">Bu komut, VirtualMachine07 adındaki sanal makine için Uzak Masaüstü dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="8ebda-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="8ebda-112">Komut, sonucu D:\remotedesktopfile07.rdpadındaki dosyada depolar.</span><span class="sxs-lookup"><span data-stu-id="8ebda-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="8ebda-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ebda-113">PARAMETERS</span></span>

### <span data-ttu-id="8ebda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebda-114">-DefaultProfile</span></span>
<span data-ttu-id="8ebda-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ebda-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ebda-116">-Başlat</span><span class="sxs-lookup"><span data-stu-id="8ebda-116">-Launch</span></span>
<span data-ttu-id="8ebda-117">Bu cmdlet. rdp dosyasını aldıktan sonra uzak masaüstünü başlatıyor.</span><span class="sxs-lookup"><span data-stu-id="8ebda-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebda-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="8ebda-118">-LocalPath</span></span>
<span data-ttu-id="8ebda-119">Bu cmdlet. rdp dosyasını depolayan yerel tam yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebda-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebda-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ebda-120">-Name</span></span>
<span data-ttu-id="8ebda-121">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebda-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebda-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebda-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ebda-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebda-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebda-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebda-124">CommonParameters</span></span>
<span data-ttu-id="8ebda-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ebda-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebda-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebda-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebda-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ebda-127">INPUTS</span></span>

### <span data-ttu-id="8ebda-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8ebda-128">System.String</span></span>

## <span data-ttu-id="8ebda-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ebda-129">OUTPUTS</span></span>

### <span data-ttu-id="8ebda-130">System. void</span><span class="sxs-lookup"><span data-stu-id="8ebda-130">System.Void</span></span>

## <span data-ttu-id="8ebda-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ebda-131">NOTES</span></span>

## <span data-ttu-id="8ebda-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ebda-132">RELATED LINKS</span></span>
